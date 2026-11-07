# NOTES: Dog health and diet

## Scope
- Topic: dog health and diet (nutrition, feeding, food selection and labels, obesity, toxic foods, special diets such as raw, vegan and home-cooked, and core preventive health).
- Defaults: all audiences (owners first), the most current resources, English, any region.
- Date: 2026-11-07.

## Weights
Default weights were used (Relevance 20, Reliability 20, Authority 15, Depth 15, Accuracy 10, Practical 10, Currentness 5, Community 5). Veterinary nutrition guidance changes slowly, so currentness was not raised.

## Access preflight (curl, this session)
| Category | Hosts | Result |
|---|---|---|
| Primary/official | wsava.org, fda.gov (pages), aafco.org, capcvet.org | OPEN |
| Primary/official | avma.org (Incapsula bot wall), aaha.org main site (403), cdc.gov (403), bsava.com (403) | BLOCKED |
| Academic | pmc.ncbi.nlm.nih.gov (intermittent: worked earlier, later served a reCAPTCHA for one article), vet.tufts.edu, sites.tufts.edu, vet.cornell.edu, ucdavis.edu, rvc.ac.uk, rcvsknowledge.org | OPEN |
| Academic | mdpi.com, europepmc.org, doaj.org, vetmed.ucdavis.edu, morrisanimalfoundation.org, purinainstitute.com (403) | BLOCKED |
| Communities | reddit.com (bot challenge, tested in prior session and again here) | BLOCKED |
| Community/independent | skeptvet.com, whole-dog-journal.com | OPEN |
| Reference | merckvetmanual.com, en.wikipedia.org | OPEN |
| Charities | aspca.org, pdsa.org.uk, rspca.org.uk, petobesityprevention.org | OPEN |
| Video | youtube.com | OPEN |
| Archives | web.archive.org | DEAD (timeout, prior session) |

## Excluded-source log
- BLOCKED: AVMA raw-diet policy and pet-owner pages (bot wall); AAHA life stage guidelines (403); Morris Animal Foundation Golden Retriever Lifetime Study (403); UC Davis vet nutrition service (403); CDC Healthy Pets and Salmonella (403); BSAVA (403); Purina Institute life span study page (403); DOAJ (403); MDPI and Europe PMC copies of the vegan systematic review (403); Veterinary Partner (VIN), which served a bot-protection script; Reddit.
- REPLACED IN FINAL VERIFICATION: the PMC copy of the vegan-diet systematic review (PMC9860667) served a reCAPTCHA on re-check. It was replaced with the accessible RCVS Knowledge resource page for the same review.
- DEAD/404: petmd.com/dog and /dog/nutrition; the Merck owner "nutrition in dogs" deep link; the PDSA "feeding your dog" page; pfma.org.uk (timeout); the fda.gov media PDF of the Freeman 2018 DCM commentary (abuse-detection page); the fediaf.org redirect to a "comingsoon.site" placeholder (excluded as suspicious); dogaging.org with www (timeout; the content subdomain was used instead).
- QUALITY EXCLUSIONS: content-farm "toxic foods" lists (dog.it.com, spice.alibaba.com, pawwise.it.com and similar); presentationbuilder.internationaltrucks.com (spam); brand-run "WSAVA" pages (Royal Canin, JustFoodForDogs, Natural Balance, Instinct, The Farmer's Dog), which are vendor framing of WSAVA material; spam PDFs for "Pet Nutrition Alliance" and "Dog Nutrition Manual".

## Community findings (ANECDOTAL)
Reddit was blocked, so community signals come from search-result snippets and independent sites:
- Veterinary-nutrition-literate owners repeatedly point to Tufts Petfoodology, WSAVA's "questions to ask the manufacturer", SkeptVet and Balance It/petdiets.com (board-certified nutritionists) as the trusted starting points.
- Raw-feeding advocacy sites (Raw Essentials, Little Big Cat, TruthAboutPetFood) dispute the AVMA and FDA Salmonella evidence. They are advocacy sources and are not used for ranking.
- Whole Dog Journal is popular with owners. Its ingredient-based "approved foods" criteria differ from the WSAVA approach, which centers on the manufacturer's expertise and quality control.

## Disagreements and cross-checks
- Grain-free/DCM: FDA (Q&A updated Aug 2024) has established no causal link and gives no diet-change advice for healthy dogs. Tufts nutritionists (Freeman et al.) describe a "BEG diet" association. Industry (Pet Food Institute) stresses that no causation has been found. The sources agree the evidence is unresolved.
- Raw diets: FDA, AVMA (blocked) and AAHA advise against them because of pathogen risk. Advocacy sites disagree. Consumer Reports takes a middle position (avoid if you can, otherwise handle safely).
- Vegan diets: the 2023 systematic review found limited and low-quality evidence with no clear harm in dogs. The Knight survey (owner-reported) suggested benefits but is open to bias.
- Feeding frequency: the Dog Aging Project association (once-daily feeding) is cross-sectional. The authors explicitly say it is not a feeding recommendation.
- Calorie restriction: the Purina Life Span Study (Kealy 2002) found that restricted dogs lived about 1.8 years longer. It is industry-funded, and the page was blocked, so it is not listed.
- Obesity prevalence: APOP 2022 reports 59% of dogs overweight or obese (vet-assessed). VetCompass reports 7% recorded obesity diagnoses in UK primary care. These are different measures (BCS assessment vs. recorded diagnosis).
- Merck's nutrient profiles were criticized as outdated by one advocacy site (TruthAboutPetFood). This is unverified, and Merck is still ranked on its breadth and authority.

## Deduplication decisions
- The Merck professional nutrition chapter is a near-miss; the Merck owner section was selected.
- The RVC "most common disorders" PDF infographic is a near-miss; the underlying VetCompass paper was selected.
- WSAVA Guidelines hub and WSAVA "Selecting a pet food" PDF are both kept. They are distinct documents (a guideline collection vs. an owner checklist).
