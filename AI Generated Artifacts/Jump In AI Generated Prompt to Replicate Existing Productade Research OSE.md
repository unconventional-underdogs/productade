# Prompt: GitHub Discussion Research Tool (Single-File HTML Application)

## Overview

Create a single-file HTML application that allows users to research GitHub discussions for product analysis. The tool should fetch discussion data via CORS proxies, extract key metadata, enable keyword search, and export results to CSV.

**Purpose:** Help product researchers analyze GitHub discussions to identify pain points, feature requests, and use cases from open source communities.

**Technical constraint:** Everything must be in ONE HTML file (HTML, CSS, JavaScript combined). No external frameworks. No build tools. Works by opening the file directly in a browser.

---

## Application Structure

### Section 1: Import GitHub Discussions (Headers)
- Text area for users to paste GitHub discussion listing page URLs (one per line)
- Example input: `https://github.com/owner/repo/discussions` or `https://github.com/owner/repo/discussions?page=2`
- Button: "Fetch Discussion Headers"
- Extracts from listing pages: title, author, date, votes, comments, category, link
- Shows preview of imported discussions in a table

### Section 2: Keyword Analysis
- Text area for users to enter keywords to search (one per line)
- Button: "Analyze Keywords"
- Searches through all imported discussions for keyword matches
- Counts frequency of each keyword across discussions

### Section 3: Results
- Sortable table displaying results with columns: keyword, frequency, title, author, date, votes, comments, category, excerpt, source (link)
- Button: "Download as CSV"
- Table headers should be clickable to sort ascending/descending

---

## Technical Requirements

### CORS Proxy Handling
Since browsers block direct cross-origin requests to GitHub, the app must use CORS proxies. Implement a fallback system that tries multiple proxies in sequence:

```javascript
const corsProxies = [
    u => 'https://api.allorigins.win/raw?url=' + encodeURIComponent(u),
    u => 'https://corsproxy.io/?' + encodeURIComponent(u),
];
```

Try each proxy until one succeeds. If all fail, show an error message.

### Data Extraction - Discussion Listing Pages

Extract discussions from GitHub listing pages. Handle TWO formats:

**Format 1: Markdown-style (some proxies convert HTML to markdown)**
```
* 105
   You must be logged in to vote
   
### [Discussion Title](/owner/repo/discussions/123)
[Q&A]
[username](/username) asked this question
Jan 15, 2024
[24](/owner/repo/discussions/123)
```

**Format 2: Raw GitHub HTML**
```html
<a href="/owner/repo/discussions/123" class="markdown-title">Discussion Title</a>
<button aria-label="Upvote: (105): username, date">
<span aria-label="105 comments: username, date">
```

Extraction patterns for listing pages:
- **Title:** `class="[...]markdown-title[...]">TITLE</a>` or `### [TITLE](link)`
- **Link:** href containing `/discussions/NUMBER`
- **Votes:** `aria-label="Upvote: (N):` or `N You must be logged in to vote`
- **Comments:** `aria-label="N comments:` or last `[N](/discussions/N)` in block
- **Author:** `[username](/username) asked` or `data-hovercard-type="user"`
- **Date:** `datetime="YYYY-MM-DD"` or `Mon DD, YYYY` text format
- **Category:** `[Q&A]`, `[Ideas]`, `[Show and tell]`, `[General]`, `[Announcements]`, `[Polls]`

### Data Extraction - Individual Discussion Pages

For deeper analysis, also support fetching individual discussion URLs. Extract:

- **Title:** `<title>` tag, clean up ` · Discussion #N · GitHub` suffix
- **Author:** 
  - CORS proxy HTML: `data-hovercard-type="user"[...]><span>USERNAME</span>` (nested span!)
  - Or: `data-hovercard-type="user"[...]>USERNAME`
  - Or: `class="author[...]">USERNAME`
  - Text format: `[username](/username) asked this question`
- **Date:** `datetime="YYYY-MM-DD"` attribute
- **Votes:** 
  - `aria-label="Upvote: N"` or `aria-label="Upvote: (N)"`
  - Or: `N You must be logged in to vote` (with flexible whitespace)
- **Comments:** 
  - Text: `N comments · M replies` (sum them)
  - HTML: `<span> N comments </span>` + `<span> M replies </span>` (sum them)
- **Category:** `>Q&A<` or `[Q&A]` (same categories as above)
- **Content:** Extract from `class="comment-body"` or `class="markdown-body"` divs, strip HTML tags

### Date Normalization

Normalize all dates to `Mon DD, YYYY` format for display. Handle:
- ISO format: `2024-10-07`
- Text format: `Oct 7, 2024` or `October 7, 2024`
- Relative: ignore (can't reliably convert)

### Keyword Search

- Case-insensitive matching
- Search in: title, content/excerpt
- Count frequency: how many times keyword appears across all text
- Return matching discussions with excerpt showing context around keyword

### CSV Export

Export columns: Keyword, Frequency, Title, Author, Date, Votes, Comments, Category, Excerpt, Source

Include summary rows at bottom showing total keyword appearances.

Filename format: `github-analysis-DDMMMYYYY_HHMMam.csv` (use San Francisco timezone)

---

## UI/UX Specifications

### Color Scheme (Dark Theme)
```css
--primary: #000000;
--secondary: #1a1a1a;
--accent: #2a2a2a;
--highlight: #ffcc00;  /* Yellow accent */
--text: #ffffff;
--text-muted: #999999;
--border: #333333;
```

### Typography
- Font: `'Courier New', monospace`
- Headings: lowercase
- Body text: 0.9rem base

### Layout
- Max-width container: 1200px, centered
- Sections with numbered step indicators (1, 2, 3)
- Rounded borders (8px)
- Subtle background: `rgba(22, 33, 62, 0.5)`

### Interactive Elements
- Buttons: Yellow background (#ffcc00), black text, hover darkens
- Tables: Striped rows, hover highlight, sortable headers with cursor pointer
- Scrollbars: Styled yellow thumb on dark track
- Status messages: Green for success, red for errors, yellow for progress

### Responsive
- Stack layout vertically on screens < 768px
- Horizontal scroll for wide tables on mobile

---

## JavaScript Architecture

### Key Functions

1. `importDiscussionTitles()` - Fetch listing pages, parse with `parseDiscussionListing()`
2. `importFromLinks()` - Fetch individual discussion URLs, parse with `parseFullDiscussion()`
3. `parseDiscussionListing(html)` - Extract array of discussions from listing page
4. `parseFullDiscussion(html)` - Extract single discussion details from detail page
5. `analyzeKeywords()` - Search discussions for keywords, calculate frequency
6. `displayResults()` - Render results table with sorting
7. `sortTable(column)` - Sort results by clicked column
8. `exportToCSV()` - Generate and download CSV file
9. `getSFTimestamp()` - Get San Francisco timezone timestamp for filenames
10. `normalizeDate(dateStr)` - Standardize date formats
11. `showStatus(elementId, message, type)` - Display status messages
12. `escapeHtml(text)` - Sanitize text for display

### State Management

Store imported discussions in a global array:
```javascript
let importedDiscussions = [];  // Array of {title, link, votes, comments, author, date, category, content}
let analysisResults = [];      // Array of {keyword, frequency, matches: [...]}
let currentSort = { column: null, direction: 'asc' };
```

### Error Handling

- Wrap all fetch calls in try/catch
- Show user-friendly error messages
- Continue processing remaining URLs if one fails
- Track success/error counts and display summary

---

## Testing Checklist

Before delivery, verify extraction works for:

| Field | CORS Proxy HTML | Web Fetch Text |
|-------|-----------------|----------------|
| title | ✓ | ✓ |
| author | ✓ (nested span) | ✓ (markdown link) |
| date | ✓ | ✓ |
| votes | ✓ | ✓ |
| comments | ✓ | ✓ |
| category | ✓ | ✓ |
| content | ✓ | ✓ |

Test with actual GitHub discussion URLs, not simulated data.

---

## Sample Test URLs

Listing pages:
- `https://github.com/openai/whisper/discussions`
- `https://github.com/openai/whisper/discussions?page=2`

Individual discussions:
- `https://github.com/openai/whisper/discussions/2377`
- `https://github.com/openai/whisper/discussions/2`

---

## License

Include MIT License header in HTML comment at top of file.

---

## Deliverable

Single HTML file (~1300-1400 lines) that:
1. Opens directly in browser (no server needed)
2. Fetches GitHub discussions via CORS proxies
3. Extracts all 7 fields correctly from both HTML and text formats
4. Enables keyword search with frequency analysis
5. Exports results to timestamped CSV
6. Has clean, professional dark-themed UI
7. Contains NO debug code (no console.log statements)
