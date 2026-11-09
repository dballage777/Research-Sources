# NOTES: Creating coloring books for sale on KDP and similar platforms

## Scope
- Topic: making and selling coloring books on Amazon KDP and similar platforms: Etsy, IngramSpark, Lulu, other print-on-demand services and digital-download marketplaces. Covers file specs, paper and printing, pricing and royalties, platform content and AI policies, copyright, trademark, and public-domain art sources, art tools, and selling digital printables.
- Defaults: all audiences, the most current resources, English, any region. The topic came with the task, so no narrowing question was asked.
- Date: 2026-11-09. Tools: WebSearch, plus curl and Playwright (headless Chromium) for verification.

## Weights
Changed from the default: Currentness raised from 5% to 10%, Depth lowered from 15% to 10%. Final weights: Relevance 20, Reliability 20, Authority 15, Depth 10, Accuracy 10, Practical 10, Currentness 10, Community 5.
Reason: platform rules for this topic changed many times between 2023 and 2026 (KDP's AI disclosure and three-titles-a-day cap, Etsy's Creativity Standards and AI rules, the U.S. Copyright Office AI reports), so out-of-date guidance is a real risk.

Diversity rule: KDP help pages scored highest because they are the primary source, but the top 30 is capped at 10 of them. Five KDP pages that scored high enough are listed as near-misses in SCORED_CANDIDATES.csv.

## Access preflight (curl, this session)
| Category | Hosts tested | Result |
|---|---|---|
| Primary/official | kdp.amazon.com, help.etsy.com, ingramspark.com, lulu.com, blog.lulu.com, help.lulu.com, copyright.gov, uspto.gov, loc.gov/free-to-use | OPEN |
| Primary/official | etsy.com (legal, seller-handbook and news pages: 403), help.ingramspark.com (Cloudflare), press.barnesandnoble.com (Access Denied), help.teacherspayteachers.com (Cloudflare), canva.com help (403), payhip.com (Cloudflare), federalregister.gov (bot wall; the govinfo.gov copy was open) | BLOCKED |
| Academic/scholarly | arxiv.org open. Little academic work exists on this topic, so the U.S. Copyright Office reports serve as the scholarly-grade sources. | OPEN (thin) |
| Communities | reddit.com and old.reddit.com (403). kdpcommunity.com threads return HTTP 200 but load their content by script; even headless Chromium rendered an empty body, so the content could not be checked. news.ycombinator.com is open, but HN Algolia found no relevant threads. stackexchange.com is open, but search found no relevant questions. | BLOCKED / THIN |
| Open source/technical | github.com web (400/403; the API worked but github.com pages cannot be listed), inkscape.org (403), potrace.sourceforge.net (Cloudflare), scribus.net (bot check) | BLOCKED |
| Open source/technical | docs.krita.org, gimp.org, en.wikipedia.org | OPEN |
| Independent/media | kindlepreneur.com, selfpublishingadvice.org (ALLi), authorsguild.org, publishersweekly.com, aarp.org, janefriedman.com (article paywalled) | OPEN |
| Independent/media | medium.com, axios.com, techspot.com (Cloudflare), writerbeware.blog (429) | BLOCKED |
| Video | youtube.com (oEmbed confirmed titles and channels) | OPEN |
| Archives | web.archive.org (timeout), smithsonian si.edu/openaccess (403), biodiversitylibrary.org (Cloudflare), loc.gov/pictures (Cloudflare), rawpixel.com (Cloudflare), openverse.org (Cloudflare) | BLOCKED |
| Archives | pdimagearchive.org, loc.gov/free-to-use, nypl.org, library.nyam.org, reusableart.com, commons.wikimedia.org, archive.org (home) | OPEN |

## Excluded-source log
- BLOCKED: Etsy Creativity Standards (etsy.com/legal/creativity); Etsy seller-handbook AI articles; Etsy IP and prohibited-items policies; IngramSpark help center (Manufacturing and File Setup Tips); Barnes & Noble Press; TPT help center; Canva content-license help pages; Payhip coloring-page guides; Potrace homepage (a Wikipedia article was used as an accessible stand-in, near-miss); Inkscape tracing tutorial; Medium "The Flood of AI Coloring Books"; Axios AI-books piece; TechSpot; Writer Beware (429); Smithsonian Open Access; Biodiversity Heritage Library; LOC Prints & Photographs; Rawpixel public domain; Openverse; Book Bolt; Creative Fabrica; Federal Register HTML (the govinfo.gov copy and the copyright.gov PDF were used instead); Reddit r/KDP and r/selfpublish.
- LOGIN/PAYWALL: Jane Friedman "Amazon issues new AI guidelines for KDP" (premium subscriber article). Publisher Rocket served a bot-verification page.
- CONTENT NOT VERIFIABLE: KDP Community threads ("Which paper is better for inked coloring books", "Print single sided", and "Issues with the printing quality of my coloring books") opened with HTTP 200 but rendered no content. They are excluded; the anecdotal points come from search snippets only (see below).
- DEAD/404: KDP topics GHPYE6WN4X27H9ET, G201231560, G201953910; blog.lulu.com/spread-happiness-create-your-own-coloring-book; ingramspark.com/plan-your-book/print/print-options; archive.org/details/coloringbooks; help.etsy.com 360000336247.
- QUALITY EXCLUSIONS: This topic has a lot of SEO and AI-content-farm material, much of it from vendors selling AI coloring-book generators: cbe-web.pages.dev, univers.studio / univers-studio.pages.dev, inkfluenceai.com, colorin.ai, bookcoverslab.com, kdpbuilder.com, kdpeasy.com, cambric.pages.dev, insightagent.app, lowcontentprofits.com, vappingo.com, scribecount.com, closo.co, ecombrainly.com, shulex.com, magicshot.ai, zsky.ai, rangy.ai, and blogspot "make money" posts. Also excluded: presentationbuilder.internationaltrucks.com and ava.ead.domalberto.edu.br (spam on hijacked subdomains), Scribd copies of official PDFs (mirrors), and Product Hunt tool listings. Their figures (such as "80% of coloring books sell under 10 copies/month" and $500–$5,000/month income claims) are unverified and were not used.

## Key facts cross-checked against primary sources (PASS 5)
- KDP does not usually treat coloring books as low-content. KDP's Low-Content Books page says the definition "does not typically include activity books, such as puzzle books or coloring books". Kindlepreneur (updated Dec 2025) calls them "medium content". Some vendor blogs still call coloring books low-content; they are wrong according to KDP.
- AI disclosure: KDP's Content Guidelines require disclosure of AI-generated content, defined as text, images or translations, and "AI-generated images include cover and interior images and artwork". AI-assisted content need not be disclosed. The Authors Guild (Sept 2023) confirms the policy started then.
- Upload cap: Publishers Weekly, the Authors Guild and ALLi (Sept 2023) all report a limit of three new titles a day. Two vendor blogs date it to 2024; the primary-adjacent reporting says 2023.
- Bleed: KDP trims 0.125 in (3.2 mm) from the top, bottom and outside edges. Lulu's PDF settings also use 0.125 in bleed, a 0.5 in safety margin and a 0.20 in minimum gutter. One blog's "0.375 in" figure contradicts both and was discarded.
- Paper: KDP black-ink interiors use 50–61 lb (74–90 GSM) white or cream paper; premium color uses 60–71 lb (88–105 GSM). The Lulu blog (Sept 2026) says uncoated paper is "a necessity" and recommends single-sided designs to reduce marker bleed.
- Resolution: KDP Paperback Submission Guidelines and Lulu both require a 300 DPI/PPI minimum.
- Etsy: the help center says digital items must be "made and/or designed by you", and that sellers may use AI tools "as long as they contribute their own creative input" and must disclose AI use in the listing description. Etsy is testing printed items from digital purchases (help article, 2026).
- Copyright: the USCO 2023 guidance (via the govinfo Federal Register copy and the copyright.gov PDF) and the Part 2 report (Jan 29, 2025) say purely prompt-generated images lack human authorship, while human selection, arrangement and modification can be protected.

## Community findings (ANECDOTAL)
Reddit was blocked and the KDP Community threads would not render, so these points come from search-result snippets only:
- KDP Community posters say KDP's standard paper (described as roughly 22 lb bond) bleeds with wet media such as markers. They advise printing designs on odd (right-hand) pages only. Black backing pages divide opinion: some call them a "kludge" that only partly works. Dry media (pencils, crayons) is generally reported as fine.
- Self-publishers commonly report modest earnings, sometimes about $50 a month per title, and say success depends on niche research and self-promotion. These reports are not verified.
- Authors' groups and news coverage (AARP, ALLi, the Authors Guild) describe AI-generated "slop" books, coloring books included, flooding marketplaces, which makes quality and originality matter more.

## Disagreements between sources
- Low-content status of coloring books: KDP and Kindlepreneur say they are not low-content; many vendor and SEO guides say they are.
- Minimum line weight: vendor sources range from 0.25 pt to 2–3 pt, and no primary source sets a figure. Print a proof and test.
- Single-sided versus double-sided printing: Lulu frames it as a cost-versus-bleed trade-off; community posters strongly prefer single-sided.
- Copyright protection of AI line art: the USCO says purely prompt-generated images are not protectable, while vendor blogs imply that light editing is enough. The USCO says protection depends on case-by-case human contribution.
