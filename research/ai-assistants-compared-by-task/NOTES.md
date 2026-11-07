# NOTES: General AI assistants compared by which is best for which jobs and tasks

## Scope
- Topic: General AI assistants (ChatGPT, Claude, Gemini, Copilot, Perplexity, etc.), compared by which is best for which jobs and tasks.
- Defaults: all audiences, the most current resources (2025–Nov 2026), English, any region.
- Research date: 2026-11-07. Narrowing was skipped because the topic was already narrowed earlier.

## Weight changes
- Currentness raised from 5% to 10%, because assistants and models change monthly and rankings go stale within months.
- Accuracy lowered from 10% to 5% to keep the total at 100%. Accuracy overlaps heavily with Reliability for this topic.
- Final weights: Relevance 20, Reliability 20, Authority 15, Depth 15, Accuracy 5, Practical 10, Currentness 10, Community 5.
- Selection rules: no exact duplicates (only one edition per report series, only one chart per survey). Vendor self-descriptions (pricing and plan pages) were kept out of the top 30 because they don't compare assistants, but they are listed as near-misses for feature checks.

## Access preflight (curl, this session)
| Category | Hosts tested | Result |
|---|---|---|
| Primary/official | anthropic.com, claude.com, chatgpt.com/pricing, gemini.google, microsoft.com, perplexity.ai | OPEN |
| Primary/official | openai.com, help.openai.com | BLOCKED (403) |
| Academic | arxiv.org, nber.org, hai.stanford.edu, dovepress.com | OPEN |
| Survey/research orgs | pewresearch.org, reutersinstitute, measuringu.com | OPEN |
| Communities | news.ycombinator.com, hn.algolia.com API | OPEN |
| Communities | reddit.com (JS bot challenge), ai.stackexchange.com tag pages (403) | BLOCKED |
| Open source/code | github.com | BLOCKED (403/400) |
| Benchmarks | artificialanalysis.ai, epoch.ai, labs.scale.com, swebench.com, drb.futuresearch.ai, openrouter.ai | OPEN |
| Benchmarks | arena.ai / lmarena.ai | BLOCKED (403) |
| Benchmarks | livebench.ai, kaggle.com/benchmarks | JS-only shell; content not readable, so treated as not verified |
| Media | pcmag, zdnet, tomsguide, zapier, eweek, theverge, fortune | OPEN |
| Media | nytimes.com, niemanlab.org, techrepublic.com, inkl.com | BLOCKED (403) |
| Video | youtube.com | OPEN |
| Archives | web.archive.org | DEAD (connection timeout, code 000) |

Accessible replacements: the OpenAI "How people are using ChatGPT" post is blocked, so the NBER paper is used instead. The Nieman Lab write-up is blocked, so the CJR/Tow Center original is used. The Vectara leaderboard on GitHub is blocked and was not replaced. Arena is blocked; Artificial Analysis, Scale SEAL and Epoch are used instead.

## Excluded-source log
- BLOCKED: openai.com/index/how-people-are-using-chatgpt/ (403); arena.ai/leaderboard (403); github.com/vectara/hallucination-leaderboard (403); niemanlab.org Tow Center article (403); techrepublic.com cheat sheet (Cloudflare 403); inkl.com Reddit-stacking article (403); reddit.com/r/ChatGPT, r/ClaudeAI, r/GeminiAI, r/perplexity_ai, r/LocalLLaMA (bot-challenge page); ai.stackexchange.com tag page (403); nytimes.com (403).
- DEAD: web.archive.org (timeout); bowdoin.edu AI tool guide PDF (404); tomsguide.com Gemini vs Claude 7-prompt test (404).
- NOT VERIFIABLE (JS-only): livebench.ai, kaggle.com/benchmarks. eqbench.com/creative_writing.html is listed as a near-miss because it was only partly readable.
- QUALITY EXCLUSIONS: twit.tv deep-research comparison (labeled "AI-generated, human-reviewed"); TechRadar and Notebookcheck (restate CJR and Microsoft studies); UF Business Library table (Oct 2024, outdated). Many SEO/affiliate "ChatGPT vs Claude vs Gemini 2026" blogs were also dropped: *.pages.dev, *.lovable.app, dev.to reposts, costbench, toolhalla, brandedagency, gmelius and similar. They have unverifiable "tests", outdated model names and vendor bias.
- Reddit mirror sites (reddit.sentinel-team.org and similar) were not used. They are scraped copies of a blocked source.

## Community findings (ANECDOTAL; evidence of reputation, not accuracy)
- HN "Ask HN: latest consensus on OpenAI vs Anthropic $20/month tier?" (Mar 2026, 15 comments): users praise Claude's coding and planning but complain about tight usage limits on the $20 tier. Some move to ChatGPT/Codex for higher limits.
- Search-snippet summaries of Reddit (not opened, because Reddit is blocked, and not used for ranking) repeat a "stack your tools" pattern: Claude for code and writing, ChatGPT for general chat and drafting, Gemini for Google and phone use, Perplexity for research.
- arXiv 2603.25220 (388 users) gives a survey-based version of the same pattern: more than 80% use two or more platforms, and satisfaction is statistically similar across Claude, ChatGPT and DeepSeek.

## Cross-checks and disagreements between sources
- "Most used": Pew (Feb 2026, US adults) has ChatGPT 44%, Gemini 24%, Copilot 17%, Claude 6%. Menlo (2026, US AI users) has ChatGPT 60%, Gemini 58%, Claude 20%. The populations differ (all adults vs. AI users), and Menlo is an Anthropic investor, so weigh its Claude figure with care. a16z (Jan 2026 traffic) has ChatGPT about 2.7x Gemini on web. All three agree ChatGPT leads in reach.
- "Best for X": the media roundups (PCMag Aug 2026, Zapier Oct 2026, ZDNET Feb 2026, eWeek Apr 2026) broadly agree. ChatGPT is best overall or general-purpose. Claude is best for writing, coding and long documents. Gemini is best for value or Google users. Copilot is best for Microsoft/Windows users. Perplexity is best for search with citations. PCMag ranks Claude only as "Best ChatGPT alternative", while Zapier ranks it "Writing and coding".
- Research accuracy: the CJR/Tow Center study (Mar 2025) found Perplexity had the lowest citation error (37%) among the tools tested. It predates current models.
- Benchmarks: Artificial Analysis, Scale SEAL and Epoch report different leaders depending on index version and date. Search summaries contradicted each other on Artificial Analysis versions, so use the live pages.
- Mollick (Jul 2026): for low-stakes chat, any assistant, including free models, is fine. For serious work, pick a frontier model, app and harness.

## Near-misses
See SCORED_CANDIDATES.csv. Notable near-misses: Mollick's Feb 2026 guide (superseded), the Anthropic June 2026 report (covered by the hub), the official pricing pages, the Reuters Institute DNR 2026, tech.co and Fortune (dated), and the Aider leaderboard (stale, Nov 2025).
