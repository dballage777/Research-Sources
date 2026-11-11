# NOTES: Evidence-based self-help for stress and anxiety, and safety rules for AI wellness chatbots

## Scope (from the user)
- Focus: coping plans, safe limits, crisis handling (988 Suicide & Crisis Lifeline), and when to send someone to a professional.
- Preferred sources: NIMH, American Psychological Association, SAMHSA, 988 Lifeline, CBT sources, and guidance on AI wellness apps.
- Defaults: all audiences, the most current resources, English, any region. Date: 2026-11-11.
- Safety note: these resources inform, they don't treat. Anyone in immediate danger should call or text 988 (US) or local emergency services.

## Weights
Currentness raised from 5% to 10% because AI-chatbot guidance and regulation changed rapidly in 2025–2026. Accuracy lowered from 10% to 5%. Final weights: Relevance 20, Reliability 20, Authority 15, Depth 15, Accuracy 5, Practical 10, Currentness 10, Community 5.
Selection followed the scores strictly. Only true duplicates were removed (for example, the 988 "Get Help" subpage and the SAMHSA 988 fact sheet PDF).

## Access preflight (curl, this session)
| Category | Hosts | Result |
|---|---|---|
| US government | nimh.nih.gov, samhsa.gov, fda.gov (pages and PDFs), ptsd.va.gov, findtreatment.gov | OPEN |
| US government | cdc.gov (403), ftc.gov (404 on root and press release; treated as blocked) | BLOCKED |
| Professional associations | psychiatry.org, beckinstitute.org | OPEN |
| Professional associations | apa.org (American Psychological Association; Incapsula bot wall on every page) | BLOCKED |
| Crisis services | 988lifeline.org, crisistextline.org, veteranscrisisline.net, thetrevorproject.org, 988.ca, findahelpline.com | OPEN |
| International/clinical | who.int, nhs.uk, nice.org.uk, cci.health.wa.gov.au | OPEN |
| Journals | arxiv.org, pmc.ncbi.nlm.nih.gov | OPEN |
| Journals | psychiatryonline.org, ai.nejm.org, jamanetwork.com, thelancet.com, healthaffairs.org (403); mental.jmir.org (202, empty) | BLOCKED |
| Nonprofits | nami.org, jedfoundation.org, mhanational.org, afsp.org, commonsensemedia.org | OPEN |
| Nonprofits | adaa.org (403), mind.org.uk (403) | BLOCKED |
| Consumer health media | mayoclinic.org (403), verywellmind.com (402) | BLOCKED |
| Communities | reddit.com (bot challenge) | BLOCKED |
| Archives | web.archive.org | DEAD (timeout) |

## Accessible-version substitutions
- The APA (American Psychological Association) Health Advisory on GenAI chatbots and wellness apps (Nov 2025) is blocked on apa.org. It is listed through the identical official PDF (author metadata "American Psychological Association", created 10 Nov 2025, 16 pages) hosted by the Consejo General de la Psicología de España (infocop.es). The EurekAlert copy of the APA press release is a near-miss (duplicate).
- The RAND/Psychiatric Services study (Aug 2025) on chatbot answers to suicide questions is blocked at psychiatryonline.org. No accessible primary copy was found, so it is not listed. Findings from news coverage are recorded below as context.
- The NEJM AI Therabot RCT (Heinz et al., 2025) is blocked. The Dartmouth news release was opened and scored; it fell just below the cutoff (7.65).

## Excluded-source log
- BLOCKED: all apa.org pages (stress tips, anxiety topic, advisory page, press release); ADAA; Mind (UK); Mayo Clinic; Verywell Mind; CDC mental health; FTC 6(b) companion-chatbot press release; Psychiatric Services RAND study; NEJM AI; JAMA Network; Lancet; Health Affairs; JMIR Mental Health; Newswise copy of the APA release; Reddit.
- REDIRECT/THIN: Anxiety Canada and MindShift pages (JS shell only); One Mind PsyberGuide (last updated 2024; maintenance unclear).
- QUALITY EXCLUSIONS: commercial safety-plan template sites (Pabau, Carepatron, Crown Counseling, Mentalyc) adapting the Stanley-Brown form; the shapes.inc "988 Lifeline avatar" (an unaffiliated AI character claiming SAMHSA ties); callsphere.ai and aiselect-chat pages (unsourced); getcoai mirrors.

## Key findings and cross-checks
- Self-help that works: CBT-based guided or unguided self-help (CCI workbooks, NHS Every Mind Matters), ACT-based WHO "Doing What Matters" (RCT-tested as guided self-help), breathing and relaxation, sleep, exercise and social connection (NIMH, NHS). NICE CG113 places self-help and guided self-help as step 2 for GAD, with escalation to high-intensity CBT or medication if symptoms persist.
- When to seek a professional: NIMH's stress fact sheet says to get help when stress or anxiety lasts, interferes with daily life, or causes avoidance, or when you are struggling to cope. Use 988 immediately for thoughts of self-harm. SAMHSA notes that most 988 contacts are resolved without emergency dispatch; call 911 for imminent danger.
- Coping and safety plans: the Stanley-Brown Safety Planning Template has six steps (warning signs, internal coping, social distraction, people to ask for help, professionals and crisis lines, making the environment safe). The template is copyrighted; reuse terms are on the form.
- AI chatbot safety rules (consensus across APA advisory, JED, FDA DHAC, Common Sense Media, Stanford, PHCC):
  1. Don't use general-purpose chatbots or wellness apps as a substitute for psychotherapy. At most, use them as an adjunct.
  2. They must detect distress, including over long conversations, and hand off to 988 or Crisis Text Line, with no method information or role-play about self-harm.
  3. No posing as a licensed professional. Disclose that the user is talking to AI.
  4. Protect sensitive data; use safe-by-default settings for minors; JED recommends no emotionally responsive companion bots for under-18s.
  5. Watch for sycophancy and dependency.
  6. Independent evaluation, adverse-event reporting and continuous monitoring (FDA DHAC).
- Evidence on AI benefit is limited. A single RCT (Therabot, NEJM AI 2025, waitlist control, n=210) showed symptom reductions with clinician oversight. The Stanford/FAccT 2025 study found stigma and unsafe crisis responses in therapy bots. The RAND study (Aug 2025, news coverage only) found inconsistent answers to intermediate-risk suicide questions. Common Sense Media found "missed breadcrumbs" that worsen in longer chats.
- Regulation (context; DLA Piper analysis was a near-miss): Illinois (HB 1806) and Nevada (AB 406) bar AI from providing therapy. Utah (HB 452) requires disclosure and data limits. California SB 243 requires companion-chatbot suicide protocols and 988-type referrals. FTC opened a 6(b) study of companion chatbots in Sept 2025 (press release blocked).

## Community findings (ANECDOTAL)
Reddit was blocked. The anecdotal signals came from news coverage summarized in search results: young people commonly use chatbots for emotional support (Common Sense: 72% of teens have used AI companions), and users report a mix of comfort and harm. These are not used for ranking.

## Disagreements
- Value of AI support: industry and some researchers point to access benefits (Therabot RCT). The APA advisory, JED and Common Sense Media say current evidence and safeguards are insufficient, especially for youth.
- Guided vs unguided self-help: meta-analyses (search summaries) suggest similar symptom outcomes, with guidance improving completion. NICE prefers guided self-help.
