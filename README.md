# Productade Research, Open Source Edition (OSE)

Welcome to the Productade Research, Open Source Edition (OSE). 

Productade Research OSE is a lightweight productivity application that 1) eases product research workflows, 2) prioritizes data provenance, and 3) supports cross-team alignment on product-market fit. Productade Research OSE is a limited and lightweight version that draws inspiration from proprietary Productade applications. Productade applications originate from intense real world experience identifying and aligning teams at the intersection of emerging technologies and product-market fit. 

![Screenshot of Product Research OSE](https://github.com/unconventional-underdogs/productade/blob/main/Images/Productade%20Research%20OSE.png)

Productade Research OSE is made available as a learning, or education, example for doing personal research on Github Discussions. Productade Research OSE is intended to help product professionals 1) obtain understanding of LLMs capabilities while building their own personal prototype applications and 2) see a tangible example of built-in traceable data provenance that supports cross-team alignment conversations and mitigate LLM hallucinations. We encourage product professionals to build their own prototypes. We offer Productade Research OSE to help save time, ease workflows, and provide a starting point.  

This readme includes the following sections:
- [Getting Started](https://github.com/unconventional-underdogs/productade/tree/main#getting-started)
- [FAQ](https://github.com/unconventional-underdogs/productade/tree/main#faq-1)
- [Resources](https://github.com/unconventional-underdogs/productade/tree/main#resources)

## Getting Started 

Humans have different preferences for learning paths and getting started. Multiple options are provided: 
- Download and Use Productade Research
- Build a Prototype Using a Human Created Natural Language Prompt
- “Jump In…Build a Personal Prototype Research App” (Using a Contextual Friendly Tutorial)
- Build a Prototype Using an AI Generated Prompt 

Choose your own adventure. 

###  Download and Use Productade Research OSE
![Screenshot of GitHub Download Raw File](https://github.com/unconventional-underdogs/productade/blob/main/Images/Github%20Download%20Raw%20File.png)

If you have a GitHub account, you can [clone](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository), [fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) or download the raw file. To download the raw file, click on “productade research_ose.html” which will open to a new dashboard that shows the HTML. Then, hover or click on the download icon near the top of the screen to “Download raw file” to a local directory. This will allow you to immediately engage with the fully rendered “productade research_ose.html” in your browser. 

If you do not have a Github account and do not want to create a free account, then 
- take your cursor and hover over the file: “productade research_ose.html”
- right-click to open the menu
- click "Save As"
- save the “productade research_ose.html” to a directory/folder on your local machine

While this will provide you with the HTML, it will be rendered in the GitHub dashboard. Yet, you can select the HTML and copy it into your preferred HTML editor. 

![Screenshot Getting Started HTML Code Selected](https://github.com/unconventional-underdogs/productade/blob/main/Images/Getting%20Started%20HTML%20Selected.png)

If you do not have a preferred HTML editor, then visit the free [W3Schools HTML Editor](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_editor)

![Screenshot W3Schools 1](https://github.com/unconventional-underdogs/productade/blob/main/Images/W3Schools_1.png)

Then, copy and paste all of the Productade Research OSE HTML into the left window and click the “Run” button. 

![Screenshot W3Schools 2](https://github.com/unconventional-underdogs/productade/blob/main/Images/W3Schools_2.png)

For learning purposes, you can also test by inserting a github discussion link, click “fetch discussion headers”. 

![Screenshot W3Schools 3](https://github.com/unconventional-underdogs/productade/blob/main/Images/W3Schools_3.png)

Then you insert a word or phrase and click “analyze keywords & phrases”.

![Screenshot W3Schools 4](https://github.com/unconventional-underdogs/productade/blob/main/Images/W3Schools_4.png)

If you would like to make saved changes, go further, or download a rendered file, then you can create a free account at W3Schools. After completing a free account you can “save the code to W3Schools Spaces”. Then edit or download the fully rendered “productade research_ose.html”. If you click on the download icon in W3Schools Spaces, W3Schools will send you an email when the zip file is ready for download.  

### Build a Prototype Using a Human Created Natural Language Prompt

Get started quickly by using a human created prompt. This prompt has been tested and fine-tuned in Anthropic Claude’s paid and free plans. As this is a “one-shot” prompt, it includes details that may not typically appear in a n’s first prompt into the large language model (LLM) on a project. 

#Prompt Begins

I am an experienced product manager and researcher for products that service machine learning engineers, data scientists and researchers. I am conducting personal research on a specific niche cohort. I would like to build a prototype lightweight html-based app for my personal use. I want a simple single html page output that I can open on my local machine and be able to open, view, and engage within a Chrome browser window. The single page html application should just work when I open it in a Chrome browser. The application should have 3 sections. Section 1 allows me to manually paste in urls/links into a window that directly imports community posts/comments/threads from specific community urls and shows when the status is complete. For section 1 in the “import” section of the app, I would like the user to have multiple options that include a) after clicking the “import” button, the app automatically fetches/imports the discussion “topics” associated with the link. Maximum of 100 urls. b) after clicking the “import” button, the app automatically fetches/imports the entire single discussion/thread. Maximum of 100 urls. Enable fetching/importing function from pasted urls using CORS proxy service such as  https://api.allorigins.win/raw?url=, https://corsproxy.io/?, or https://api.codetabs.com/v1/proxy?quest=. If the initial try fails, then try an alternate proxy. Section 2 allows the user to provide the app with keywords and phrases to find frequency within the corpus of posts extracted and show me the status of when it is complete. Section 3 provides an output that is a text table that includes date of post, the key words/phrases, frequency, “topic” or post/thread/discussion header, 250 character excerpt of where the keyword appears, author of the individual post, votes, comments, and a link to the post. Users will be able to sort the table by keyword/phrase, frequency, date, etc. Section 3 also has a “download” csv file function. The user should be able to immediately use the csv file and ensure the csv file include frequency totals. In the csv, the link/url to the post that appeared in section 1, should appear as the source. When providing the app file for me, ensure that there is a timestamped suffix.

#Prompt Ends  

#### Troubleshooting 

While the human created natural language prompt was extensively tested and fine-tuned, LLMs outputs are probabilistic. If the LLM is having challenges/overthinking or potentially overfitting on a single component, then you can “nudge” or “guide” the LLM by providing the LLM with “productade research_ose.html”  and requesting that the LLM use the “productade research_ose.html” as a reference. 

### “Jump In…Build a Personal Prototype Research App” 

This [friendly chatty contextual tutorial](https://unconventionalunderdogs.blog/2026/03/08/jump-in-build-a-personal-prototype-research-app/) helps n professionals understand the how and why associated with building a personal productivity app. The tutorial development was caffeine-powered and no “AI” was used (or harmed) for the writing of the tutorial. “AI” was used to test the natural language “cold start” prompts to ensure that the prompts work on a “free” user plan. A n reviewed the outputs and manually tweaked prompt language to increase likelihood of consistent outputs. Automated spelling and grammar check tooling was used to proactively protect dearest readers and learners from epic typos. This tutorial originally appeared on the unconventional underdogs blog. In the future, it may be placed in the “Wiki” or similar section because the Wiki section is not immediately sucked up by bots. The “Jump In” tutorial, after all, is intended for dearest n readers and learners. 

### Build Prototype Using an AI Generated Prompt 

If looking to “cut-and-paste” a detailed or “enterprise” prompt into a commercial large language model (LLM) or AI-assisted builder without context, then [this prompt is for you](https://github.com/unconventional-underdogs/productade/tree/main/AI%20Generated%20Artifacts). After Productade Research OSE v 0.1 was completed, the app code was inserted into a commercial LLM and prompted to generate a prompt for future learners to immediately create their own versions to immediately engage. 

### FAQ

If looking for specific contextual facts with no chatty fluff to get, then visit the FAQ. It is written with a “docs” approach and tone. unconventional underdogs are well aware that many humans prefer going directly to “docs” to understand the “who”, “what”, “why”, and “how”, before making any decisions about investing additional intellectual capital. The FAQ addresses this common use case. 

# FAQ

### Q. What is Productade?  
Productade is a family of productivity applications for product people that still want to use their brains. 

#### Q. What are Productade applications?  
Productade applications help accelerate product workflows. 

#### Q. What is Productade Research OSE?   
Productade Research OSE is a lightweight productivity application to ease product research workflows. unconventional underdogs developed various proprietary productivity applications to help accelerate product research while prioritizing data provenance. Prioritizing data provenance supports product-market fit and cross-alignment tradeoff discussions amongst multiple invested teams. unconventional underdogs decided to open source a limited feature application to help other product-oriented people ease their workflows and support maintaining credibility with paired data provenance. See [artifacts](https://github.com/unconventional-underdogs/productade/tree/main?tab=readme-ov-file#artifacts) for specific evidence on why there is a need for people to share upskilling insights, tooling, and best practices. 

#### Q. Why is it called Producatade?   
"Productade" is a uniquely created word. Productade is a play on "product aide", "product assistant", as well as the suffix "ade", a refreshing beverage. Productade applications aim to be helpful refreshing options.

#### Q. Who developed Productade?   
[unconventional underdogs](https://unconventionalunderdogs.com/) developed Productade.  

#### Q. What are unconventional underdogs?  
[unconventional underdogs](https://unconventionalunderdogs.com/) focus on building bridges and tunnels to emerging technologies. unconventional underdogs was founded on the belief that technical excellence, product insight, and helpful products don't have to be separate universes. We understand the complexity involved when building emerging, and potentially, disruptive products. We also have deep experience working with technical founders that are akin to unicorns, dragons, and sabertooth tigers. We are here to help and enable, not control.

#### Q. How do I get started?  
Humans have different preferences for learning paths and getting started with new emerging technologies. Choose your own adventure. 

##### Build a Prototype Using a Human Created Natural Language Prompt

Get started quickly by using a human created prompt. This prompt has been tested and fine-tuned in Anthropic Claude’s paid and free plans. As this is a “one-shot” prompt, it includes details that may not typically appear in a human’s first prompt into the LLM on a project. 

#Prompt Begins

I am an experienced product manager and researcher for products that service machine learning engineers, data scientists and researchers. I am conducting personal research on a specific niche cohort. I would like to build a prototype lightweight html-based app for my personal use. I want a simple single html page output that I can open on my local machine and be able to open, view, and engage within a Chrome browser window. The single page html application should just work when I open it in a Chrome browser. The application should have 3 sections. Section 1 allows me to manually paste in urls/links into a window that directly imports community posts/comments/threads from specific community urls and shows when the status is complete. For section 1 in the “import” section of the app, I would like the user to have multiple options that include a) after clicking the “import” button, the app automatically fetches/imports the discussion “topics” associated with the link. Maximum of 100 urls. b) after clicking the “import” button, the app automatically fetches/imports the entire single discussion/thread. Maximum of 100 urls. Enable fetching/importing function from pasted urls using CORS proxy service such as  https://api.allorigins.win/raw?url=, https://corsproxy.io/?, or https://api.codetabs.com/v1/proxy?quest=. If the initial try fails, then try an alternate proxy. Section 2 allows the user to provide the app with keywords and phrases to find frequency within the corpus of posts extracted and show me the status of when it is complete. Section 3 provides an output that is a text table that includes date of post, the key words/phrases, frequency, “topic” or post/thread/discussion header, 250 character excerpt of where the keyword appears, author of the individual post, votes, comments, and a link to the post. Users will be able to sort the table by keyword/phrase, frequency, date, etc. Section 3 also has a “download” csv file function. The user should be able to immediately use the csv file and ensure the csv file include frequency totals. In the csv, the link/url to the post that appeared in section 1, should appear as the source. When providing the app file for me, ensure that there is a timestamped suffix.

#Prompt Ends  

###### Troubleshooting 

While the human created natural language prompt was extensively tested and fine-tuned, LLMs outputs are probabilistic. If the LLM is having challenges/overthinking or potentially overfitting on a single component, then you can “nudge” or “guide” the LLM by providing the LLM with “productade research_ose.html”  and requesting that the LLM use the “productade research_ose.html” as a reference. 

##### “Jump In…Build a Personal Prototype Research App” 

This [friendly chatty contextual tutorial](https://unconventionalunderdogs.blog/2026/03/08/jump-in-build-a-personal-prototype-research-app/) helps human professionals understand the how and why associated with building a personal productivity app. The tutorial development was caffeine-powered and no “AI” was used (or harmed) for the writing of the tutorial. “AI” was used to test the natural language “cold start” prompts to ensure that the prompts work on a “free” user plan. A human reviewed the outputs and manually tweaked prompt language to increase likelihood of consistent outputs. Automated spelling and grammar check tooling was used to proactively protect dearest readers and learners from epic typos. This tutorial originally appeared on the unconventional underdogs blog. In the future, it may be placed in the “Wiki” or similar section because the Wiki section is not immediately sucked up by bots. The “Jump In” tutorial, after all, is intended for dearest human readers and learners. 

##### Build Prototype Using an AI Generated Prompt 

If looking to “cut-and-paste” a detailed or “enterprise” prompt into a commercial large language model (LLM) or AI-assisted builder without context, then [this prompt is for you](https://github.com/unconventional-underdogs/productade/tree/main/AI%20Generated%20Artifacts). After Productade Research OSE v 0.1 was completed, the app code was inserted into a commercial LLM and prompted to generate a prompt for future learners to immediately create their own versions to immediately engage. 

##### FAQ

This FAQ. If looking for specific contextual facts with no chatty fluff to get, then visit the FAQ. It is written with a “docs” approach and tone. unconventional underdogs are well aware that many humans prefer going directly to “docs” to understand the “who”, “what”, “why”, and “how”, before making any decisions about investing additional intellectual capital. The FAQ addresses this common use case. 

#### Q. Why and how is Productade Research OSE different?  
Productade applications are for humans that still want to use their brains to ensure their skills do not [atrophy](https://x.com/karpathy/status/2015883857489522876). Product people, in particular, are required to continuously observe, understand, and learn about users in order to best help them. Productade applications help accelerate workflows and keep “humans-in-the-loop”.   

Productade also prioritizes data provenance to help reinforce credibility and support cross-functional team alignment on complex products. Productade applications consider real world experience delivering products in high stakes situations, where data provenance is a "must have" not a "nice to have". While various large language models (LLMs) or “AI” have “summarization” capabilities, many are not able to pinpoint specific sources which leads to hallucinations. 

#### Q. What is the AI use policy?   
unconventional underdogs provide transparency on the AI use for any artifacts. 

#### Q. Language is repeated in the Readme. Why?    
Based on observing humans engaging with product documentation online, it is likely that humans will reference specific sections as needed and not look at other sections. Hence, we made the design choice to repeat certain paragraphs to ease user discoverability and support their learning journey. 


# Resources
## Productade Artifacts
Contextual introductions, hands-on guides, and actionable insights to help product people broker alignment and make their own tradeoff decisions 

| Title | Source |
|-------|--------|
| "Jump In…Build A Personal Prototype Research App" | [Link](https://unconventionalunderdogs.blog/2026/03/08/jump-in-build-a-personal-prototype-research-app/) | 
| "All About The Context: A Contextual First Step Into Building With LLMs Or AI" | [Link](https://unconventionalunderdogs.blog/2026/03/25/all-about-the-context/) |

## Institutional, Industry, and Academic Artifacts
Specific evidence on "why" there is a need share insights, tips, and best practices on working with AI. 

| Date | Title | Source |
|------|-------|--------|
| Apr 2026 | "Sam Altman May Control Our Future - Can He Be Trusted?" | New Yorker [Link](https://www.newyorker.com/magazine/2026/04/13/sam-altman-may-control-our-future-can-he-be-trusted) |
| Apr 2026 | "Why Some Employees Are Feeling Overwhelmed By Having To Use AI At Work" | CNBC [Link](https://www.youtube.com/watch?v=Cp0-Yu31uJ4) |
| Apr 2026 | "LLM Knowledge Bases" | Karpathy X Post [Link](https://x.com/karpathy/status/2039805659525644595) |
| Mar 2026 | "Peer-Preservation in Frontier Models: Emergent misaligned behaviors in multi-agent systems" | UC Berkeley [Link](https://rdi.berkeley.edu/blog/peer-preservation/) |
| Mar 2026 | "Number of AI chatbots ignoring human instructions increasing, study says. Exclusive: Research finds sharp rise in models evading safeguards and destroying emails without permission" | Guardian [Link](https://www.theguardian.com/technology/2026/mar/27/number-of-ai-chatbots-ignoring-human-instructions-increasing-study-says) |
| Mar 2026 | "As Trump rolls back protections, Governor Newsom signs first-of-its-kind executive order to strengthen AI protections and responsible use" | CA State Press Release [Link](https://www.gov.ca.gov/2026/03/30/as-trump-rolls-back-protections-governor-newsom-signs-first-of-its-kind-executive-order-to-strengthen-ai-protections-and-responsible-use/) |
| Mar 2026 | Executive Department State of California "EXECUTIVE ORDER N-5-26" | EXECUTIVE ORDER N-5-26 [Link](https://www.gov.ca.gov/wp-content/uploads/2026/03/3.30-FINAL-Trusted-AI-Procurement-EO-N-5-26.pdf) |
| Mar 2026 | "Coding After Coders: The End of Computer Programming as We Know It" | NYTimes [Link](https://www.nytimes.com/2026/03/12/magazine/ai-coding-programming-jobs-claude-chatgpt.html?unlocked_article_code=1.S1A.Wj2I.GFnB7ufQCCrA&smid=url-share) |
| Mar 2026 | "Amazon convenes ‘deep dive’ internal meeting to address outages" | CNBC [Link](https://www.cnbc.com/2026/03/10/amazon-plans-deep-dive-internal-meeting-address-ai-related-outages.html) |
| Mar 2026 | "Claude outages lay bare software developers' growing reliance on AI: 'I guess I'll write code like a caveman'"| Business Insider [Link](https://www.businessinsider.com/claude-outages-anthropic-ai-software-engineers-developers-coding-dependance-2026-3) |
| Mar 2026 | "When Using AI Leads to “Brain Fry" | Harvard Business Review [Link](https://hbr.org/2026/03/when-using-ai-leads-to-brain-fry) |
| Mar 2026 | "You’ve Finally Figured Out AI at Work—Now Comes the Bill" | WSJ [Link](https://www.wsj.com/tech/ai/ai-tokens-productivity-d35c6bd8?st=C7CA9r&reflink=desktopwebshare_permalink) | 
| Mar 2026 | "Meta is having trouble with rogue AI agents" | TechCrunch [Link](https://techcrunch.com/2026/03/18/meta-is-having-trouble-with-rogue-ai-agents/) | 
| Mar 2026 | "The Hottest Job in Tech Isn’t Very Glamorous: Job postings for ‘forward deployed engineers’ are surging among tech companies. But engineers aren’t exactly clamoring for the role." | WSJ [Link](https://www.wsj.com/cio-journal/the-hottest-job-in-tech-isnt-very-glamorous-dc29ab3e) |
| Mar 2026 | "Microsoft Seeks More Coherence in AI Efforts With Copilot Reorganization" | WSJ [Link](https://www.wsj.com/tech/ai/microsoft-seeks-more-coherence-in-ai-efforts-with-copilot-reorganization-a985b374?mod=WTRN_pos5) |
| Mar 2026 | "OpenAI preps for IPO by end of year, tells employees ChatGPT must be ‘productivity tool’"| CNBC [Link](https://www.cnbc.com/2026/03/17/openai-preps-for-ipo-in-2026-says-chatgpt-must-be-productivity-tool.html) | 
| Feb 2026 | "The Siren Song of LLMs: How Users Perceive and Respond to Dark Patterns in Large Language Models", Created Sept 2025, Last Updated Feb 2026, | Accepted Paper to CHI '26 in April 2026 [Link](https://arxiv.org/abs/2509.10830) |
| Feb 2026 | "Companies replaced entry-level workers with AI. Now they are paying the price." | Fast Company [Link](https://www.fastcompany.com/91483431/companies-replaced-entry-level-workers-with-ai) |
| Feb 2026 | "The Lesson of A.I. Literacy Class: Don’t Let the Chatbot Think for You" | NYTimes [Link](https://www.nytimes.com/2026/02/23/technology/ai-literacy-newark-school-chatbots.html) |
| Feb 2026 | "Most Americans say AI will reduce the number of jobs in the U.S." | YouGov Survey [Link](https://today.yougov.com/technology/articles/54123-most-americans-say-ai-artificial-intelligence-will-reduce-number-jobs-in-us-united-states-february-13-16-2026-economist-yougov-poll) |
| Feb 2026 | "AI Doesn't Reduce Work—It Intensifies It" | Harvard Business Review [Link](https://hbr.org/2026/02/ai-doesnt-reduce-work-it-intensifies-it) |
| Feb 2026 | "AI promised to free up workers' time. UC Berkeley Haas researchers found the opposite." | UC Berkeley [Link](https://newsroom.haas.berkeley.edu/ai-promised-to-free-up-workers-time-uc-berkeley-haas-researchers-found-the-opposite/) |
| Feb 2026 | "Amazon’s cloud ‘hit by two outages caused by AI tools last year’" | Guardian [Link](https://www.theguardian.com/technology/2026/feb/20/amazon-cloud-outages-ai-tools-amazon-web-services-aws) |
| Jan 2026 | "In the future, do you think that when AI tools recommend products, they will more often prioritize...?" | YouGov Survey [Link](https://today.yougov.com/topics/technology/survey-results/daily/2026/01/15/24a57/4) |
| Jan 2026 | "A few random notes from claude coding quite a bit last few weeks." | Karpathy X Post [Link](https://x.com/karpathy/status/2015883857489522876) |
| Jan 2026 | "Hospitals Are a Proving Ground for What AI Can Do, and What It Can't" | WSJ [Link](https://www.wsj.com/tech/ai/hospitals-are-a-proving-ground-for-what-ai-can-do-and-what-it-cant-60e4020c) |
| Jan 2026 | "Learning the Wrong Lessons: Syntactic-Domain Spurious Correlations in Language Models", Paper Published Sept 2025, Last Modified Jan 2026  | NeurIPS 2025 [Link](https://neurips.cc/virtual/2025/loc/san-diego/poster/116066) |
| Dec 2025 | "How AI coding agents work—and what to remember if you use them" | Ars Technica [Link](https://arstechnica.com/information-technology/2025/12/how-do-ai-coding-agents-work-we-look-under-the-hood/) |
| Dec 2025 | "AI Use at Work Rises" | Gallup [Link](https://www.gallup.com/workplace/699689/ai-use-at-work-rises.aspx) |
| Dec 2025	| "Are these AI prompts damaging your thinking skills?" |	BBC [Link](https://www.bbc.com/news/articles/cd6xz12j6pzo) |
| Dec 2025| "Microsoft stock sinks on report AI product sales are missing growth goals"	| CNBC [Link](https://www.cnbc.com/2025/12/03/microsoft-stock-ai-foundry-sales.html#:~:text=Microsoft%20pushed%20back%20on%20a,concepts%20of%20growth%20and%20quotas.)
| Nov 2025 | "How are Americans using AI? Evidence from a nationwide survey." | Brookings [Link](https://www.brookings.edu/articles/how-are-americans-using-ai-evidence-from-a-nationwide-survey/) |
| Nov 2025 | "The state of AI in 2025: Agents, innovation, and transformation" | Mckinsey [Link](https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai#/) |
| Nov 2025 | "Researchers discover a shortcoming that makes LLMs less reliable" | MIT News [Link](https://news.mit.edu/2025/shortcoming-makes-llms-less-reliable-1126) |
| Nov 2025 | "Microsoft faces uphill climb to turn enterprise dominance into widespread AI chatbot adoption" | CNBC [Link](https://www.cnbc.com/2025/11/23/microsoft-faces-uphill-climb-to-win-in-ai-chatbots-with-copilot.html) |
| Oct 2025 | "Understanding Human-AI Misalignment in LLM-Based Job-Seeking Support for Neurodivergent Users" | ACM SIGACCESS (27th) [Link](https://dl.acm.org/doi/10.1145/3663547.3746361) |
| Aug 2025 | "The GenAI Divide State of AI In Business 2025" | MIT NANDA [Link](https://mlq.ai/media/quarterly_decks/v0.1_State_of_AI_in_Business_2025_Report.pdf) |
| Aug 2025 | "MIT report: 95% of generative AI pilots at companies are failing" | Fortune [Link](https://fortune.com/2025/08/18/mit-report-95-percent-generative-ai-pilots-at-companies-failing-cfo/)
| Jul 2025 | “Measuring the Impact of Early-2025 AI on Experienced Open-Source Developer Productivity” | METR Paper [Link](https://arxiv.org/abs/2507.09089) | 
| Jul 2025 | "What Workers Really Want from Artificial Intelligence" | Stanford [Link](https://hai.stanford.edu/news/what-workers-really-want-from-artificial-intelligence) | 
| Jun 2025 | "Your Brain on ChatGPT: Accumulation of Cognitive Debt When Using an AI Assistant for Essay Writing Task" | MIT Media Lab [Link](https://www.media.mit.edu/publications/your-brain-on-chatgpt/) |	
| Jun 2025 | "+1 for "context engineering" over "prompt engineering”."| Karpathy X Post  [Link](https://x.com/karpathy/status/1937902205765607626) |	
| May 2025 | "AI and Data Regulation, 2025 Berkeley Spring Forum on M&A and the Boardroom" | UC Berkeley YouTube [Link](https://www.youtube.com/watch?v=ksBK7nnOMek) |
| May 2025 | "Copyright and Artificial Intelligence" Pre-Publication Version | U.S. Copyright Office PDF [Link](https://www.copyright.gov/ai/Copyright-and-Artificial-Intelligence-Part-3-Generative-AI-Training-Report-Pre-Publication-Version.pdf) |
| Apr 2025 | "How the U.S. Public and AI Experts View Artificial Intelligence" | Pew Research [Link](https://www.pewresearch.org/wp-content/uploads/sites/20/2025/04/pi_2025.04.03_us-public-and-ai-experts_report.pdf) |
| Apr 2025 | "Hallucination-Free? Assessing the Reliability of Leading AI Legal Research Tools" | Cornell Law School [Link](https://onlinelibrary.wiley.com/doi/10.1111/jels.12413) |
| Apr 2025 | "The 2025 AI Index Report" | Stanford [Link](https://hai.stanford.edu/ai-index/2025-ai-index-report) |
| Apr 2025 | "Artificial intelligence in daily life: Views and experiences" | Pew Research [Link](https://www.pewresearch.org/internet/2025/04/03/artificial-intelligence-in-daily-life-views-and-experiences/) |
| Jan 2025 | "Future of Jobs Report 2025" | World Economic Forum [Link](https://reports.weforum.org/docs/WEF_Future_of_Jobs_Report_2025.pdf) |
| Jan 2025 | "Experienced software developers assumed AI would save them a chunk of time. But in one experiment, their tasks took 20% longer" | Fortune [Link](https://fortune.com/article/does-ai-increase-workplace-productivity-experiment-software-developers-task-took-longer/) |
| 2025 | Stack Overflow 2025 Survey Data | Stack Overflow [Link](https://survey.stackoverflow.co/) |
| 2025 | Stack Overflow Chart: How do you choose to find relevant developer content | Stack Overflow [Link](https://survey.stackoverflow.co/2025/stack-overflow#participation-and-feedback-so-dev-content) |
| 2025 | Stack Overflow Chart: Accuracy of AI tools | Stack Overflow [Link](https://survey.stackoverflow.co/2025/ai#developer-tools-ai-acc) |
| 2025 | Stack Overflow Chart: AI tool's ability to handle complex tasks | Stack Overflow [Link](https://survey.stackoverflow.co/2025/ai#developer-tools-ai-complex) |
| 2025 | Stack Overflow Chart: AI and humans in the future | Stack Overflow [Link](https://survey.stackoverflow.co/2025/ai#developer-tools-ai-human) |
| May 2024 | "Is Temperature the Creativity Parameter of Large Language Models?" | ICCC 24, Best Student Paper [Link](https://arxiv.org/abs/2405.00492)|
| Nov 2023 | "Lost in the Middle: How Language Models Use Long Contexts" Paper Published Jul 2023, Last Modified Nov 2023 | TACL [Link](https://arxiv.org/abs/2307.03172)|

## Sites and Trackers
Additional resources for product people that need to monitor latest developments from reputable citable sources. 

| Date | Title | Source |
|------|-------|--------|
| 2026 | ACM Digital Library | [Link](https://www.acm.org/publications/digital-library) |
| 2026 | AI Hallucination Cases | [Link](https://www.damiencharlotin.com/hallucinations/) | 
| 2026 | AI Incidents Database | [Link](https://incidentdatabase.ai/) |
| 2026 | AI Law Librarians | [Link](https://www.ailawlibrarians.com/) | 
| 2026 | CourtListener | [Link](https://www.courtlistener.com/) |
| 2026 | U.S. AI Law Tracker | Orrick [Link](https://ai-law-center.orrick.com/us-ai-law-tracker-see-all-states/) |
| 2026 | US State AI Governance Legislation Tracker | iapp [Link](https://iapp.org/resources/article/us-state-ai-governance-legislation-tracker) |
