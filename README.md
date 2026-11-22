# Frictional: the paper

## Executive summary

**What this is:** the working repository for turning the Frictional preprint (*Measuring the Struggle: Process Friction Traces as Independent Evidence of Genuine Learning in the Age of Generative AI*) into peer-reviewed papers. The current draft is [paper/frictional.md](paper/frictional.md), the preprint as published on nikbearbrown.com, converted to Markdown. This README is the plan: the concrete steps, in order, with dates.

**Why read it:** the preprint makes empirical claims with no data behind them, and the data it needs come from students in your own courses. Two things have to happen before writing pays off: an IRB determination, and instruments built into next semester's courses before the first day of class. Both are on a short clock.

**What it decides:**
1. **Yes, you need IRB approval before using any student work in a paper,** including past projects. Northeastern policy 505 says faculty may not recruit students from their own classes for research without a determination from the Department of Human Research (DHR), and only the DHR can decide a study is exempt. File **one application** covering both the Fall 2026 records and the Spring 2027 courses. Drafts of every part are in [irb/](irb/).
2. **Submit by Friday, December 4, 2026.** Applications go by email to the DHR. The DHR's median turnaround for new exempt and expedited applications is 10 business days, so a December 4 submission should be decided around December 18. Spring classes start **Wednesday, January 13, 2027**.
3. **Talk to the Office of the General Counsel about FERPA too.** Northeastern's guidance says you must consult the OGC whenever research uses data that could fall under FERPA, and coursework does. A signed, IRB-approved consent form usually also satisfies FERPA.
4. **Recruit at the end of term, through a third party.** Northeastern's guidance on recruiting your own students recommends a third party, the instructor not knowing who took part, and recruiting at the end of the semester. The plan does all three: the third party collects consent in the last week of classes, and seals the forms until grades are submitted.
5. **Every Spring 2027 course gets the same core instruments.** These are confidence ratings on quizzes, coded quiz distractors, transfer items, milestone commits, the Frictional log as it is now, and a short in-class transfer check at the end of term. The one or two largest sections can also get spaced retrieval and randomized hints, but **the DHR's guidance says random assignment of students to different teaching methods "would probably not be exempt."** Those two instruments probably move the application from exempt to expedited review. That is fine for the timeline, but say so in the application. Setup checklist: [courses/README.md](courses/README.md).
6. **Two papers, not one.** Paper 1 is a framework and experience report: consented Fall 2026 cases plus AI agents completing the same assignments, claiming feasibility only. Target: the SIGCSE Technical Symposium 2028 Experience Reports and Tools track (deadline expected early July 2027). Paper 2 validates the Genuine Learning Probability (GLP) score against the in-class transfer check using Spring 2027 data. Target: LAK28 (expected late September 2027) or the Journal of Learning Analytics.
7. **One fix is due now, whatever else happens:** the published preprint says a "labeled corpus" is available at irreduciblyhuman.com. No labeled corpus exists yet. Change that sentence on the website.

**What was not done:** no IRB application was filed, nobody was contacted, no course was changed, and no student work was opened. Student folders were counted, not read. The Spring 2027 course list was not in the local files and has to be confirmed.

---

## The steps, in order

### Now to December 4, 2026 (fall break is November 25 to 29)

| # | Step | Detail | Done when |
|---|---|---|---|
| 1 | Fix the preprint's "labeled corpus" sentence on nikbearbrown.com | Put it in the future tense, or remove it. | The live page no longer says a corpus exists |
| 2 | Check your human subjects training | DHR requires the **CITI "Human Subjects Research, Stage 1 Basic Course,"** taken under the Northeastern University affiliation. It is valid for 3 years. Responsible Conduct of Research courses do not count. | Certificate valid through the end of the study (into 2028) |
| 3 | Choose the third party | A colleague or staff member who neither teaches nor grades your courses. They recruit, hold the consent forms and the code key, and de-identify the data (the "honest broker"). They need the same CITI course. | Name agreed; they have read [irb/data-management-plan.md](irb/data-management-plan.md) |
| 4 | Email the DHR with the questions below | IRBReview@northeastern.edu ([DHR site](https://dhr.research.northeastern.edu/)). Ask the seven questions in [Questions for the DHR](#questions-for-the-dhr). | Answers in hand, or a call booked |
| 5 | Email the Office of the General Counsel about FERPA | Describe the records (logs, commits, quiz responses, scores), the consent form's FERPA wording, and the honest-broker de-identification. Ask whether anything beyond the signed consent is needed. | OGC reply, or their contact named in the application |
| 6 | Confirm the Spring 2027 course list | Fill in [courses/README.md](courses/README.md#which-courses), and choose whether any section carries the full instrument set. | Table filled |
| 7 | Fill in and submit the IRB application | Use DHR's current application form, filled in from [irb/application-draft.md](irb/application-draft.md), and attach [irb/consent-form-draft.md](irb/consent-form-draft.md), [irb/recruitment-script.md](irb/recruitment-script.md), [irb/data-management-plan.md](irb/data-management-plan.md), the syllabus sentence in [courses/README.md](courses/README.md), and your CITI certificate. Add DHR's **"AI Systems Used in Human Subjects Research"** form if any AI tool will touch student data (for example, to help code logs). Email everything to IRBReview@northeastern.edu. | Submitted by **Friday, December 4** |

**Do not contact Fall 2026 students about the study** before the DHR's determination and before Fall grades are submitted (deadline: Tuesday, December 22, 2026).

### December 2026 to early January 2027 (while the DHR reviews)

| # | Step | Detail |
|---|---|---|
| 8 | Run the agent contrast | Agents complete each Fall 2026 assignment under three instructions (plain, logged, gaming), five runs each, capturing commits, logs and quiz answers. No students are involved and no IRB approval is needed. Plan: [study/agent-contrast.md](study/agent-contrast.md). This is Paper 1's comparison data and the first test of Claim 03. |
| 9 | Build the Spring 2027 item banks | Core concepts, near and far transfer pairs, misconception-coded distractors and their adjacency map, and milestone difficulty ratings. Keep it private, in this repo. Spec: [courses/instruments.md](courses/instruments.md). |
| 10 | Retroactive consent for Fall 2026 | Only after the determination **and** after December 22. The third party emails Fall 2026 students consent Version B, in the first week of January (not over the holidays), with one reminder about ten days later. Paper 1's case studies come only from students who tick the quoting or case-study boxes. |
| 11 | Start revising the paper | Begin with what does not depend on data: cut the neuroscience numbers, rebuild Section 3 on behavioral science, apply the "facet" terminology, add related work. Plan: [paper/revision-plan.md](paper/revision-plan.md). References: [paper/references-to-add.md](paper/references-to-add.md). |

### January 2027, before and just after the first class (January 13)

| # | Step | Detail |
|---|---|---|
| 12 | Build the instruments in Canvas and the course repos | Checklist in [courses/README.md](courses/README.md#before-the-first-day-of-class-every-course). Test the Canvas exports on a sandbox course. |
| 13 | Pre-register Paper 2 on OSF | Hypotheses H1 to H3, the measure definitions in [study/measures.md](study/measures.md), exclusion rules and the analysis models. It must be time-stamped before any Spring 2027 data are opened. Do it by the end of January. |
| 14 | Randomize the full-set sections, if any | After add/drop ends on **Tuesday, January 26**: two private lists, for the spaced retrieval sets and the hint versions. |

### Spring term (January 13 to April 25; spring break March 8 to 14)

| # | Step | Detail |
|---|---|---|
| 15 | Run the instruments on the calendar | The dated week-by-week table is in [courses/README.md](courses/README.md#the-term-week-by-week). |
| 16 | Keep the dated log | `courses/spring-2027-log.md`: when each instrument ran, and anything that changed. |
| 17 | Recruitment in the last week of classes (April 19 to 23) | The third party visits each class with the instructor out of the room, collects forms, and seals them until grades are submitted. |
| 18 | Write Paper 1 | Fall 2026 consented cases (Y₁, Y₂ and Y₅ only), the agent runs, and the experience of building the Spring instruments. Claim feasibility only. |

### After Spring grades (deadline Tuesday, May 4, 2027)

| # | Step | Detail |
|---|---|---|
| 19 | Honest broker opens the forms, exports and de-identifies | Consenting students only. Email follow-up to students who were absent from the recruitment visit. [irb/data-management-plan.md](irb/data-management-plan.md). |
| 20 | Analyze exactly as pre-registered | Then do any exploratory analysis, labeled as exploratory. |
| 21 | Submit Paper 1 | SIGCSE TS 2028, Experience Reports and Tools track. The deadline is not yet announced; last year's was abstracts June 26 and full papers July 3, so plan on early July 2027. Koli Calling 2027 (around mid-July) is the alternative. |
| 22 | Submit Paper 2 | LAK28 (not yet announced; last year's papers were due September 28, so plan on late September 2027), or the Journal of Learning Analytics at any time. |
| 23 | Optional: the human red-team study | People try to raise their process scores without learning the material. It needs an IRB amendment or a new protocol; the first application does not cover it. |

---

## Do you need IRB approval?

**Yes.** Publishing results built from students' coursework is research: a systematic investigation meant to produce generalizable knowledge. The students are human subjects. Northeastern adds two rules of its own. Policy 505 says faculty "may not recruit students from their classes for their own research projects unless prior approval or exemption determinations for the project have been obtained from the DHR". And exempt work cannot start until the investigator has DHR's determination letter. You cannot decide on your own that the study is exempt.

**What the application asks for:** one application, in two parts.

| Part | Data | Likely category (DHR decides) | Consent |
|---|---|---|---|
| A. Past courses (Fall 2026, possibly earlier) | Records that already exist: FRICTIONAL.md logs, commit histories, scores | Exempt, 45 CFR 46.104(d)(4)(ii): secondary use of existing records, recorded so students cannot readily be identified, no contact by the investigator, no re-identification | Requested by the third party after grades; quotes and case studies only with explicit consent |
| B. Spring 2027, core instruments | Records from activities built into the course for everyone, with no random assignment | Exempt, 46.104(d)(1): normal educational practices in an established educational setting, not likely to harm students' opportunity to learn | Opt-in, collected by the third party in the last week of class and sealed until grades are submitted |
| B'. Spring 2027, randomized instruments (spaced retrieval sets and hint versions), if used | The same, plus random assignment of students to concept sets and hint types | **Probably not exempt.** DHR's guidance says a study that "randomly assigns students to different instructional strategies/curricula for comparison, would probably not be exempt." Expect expedited (minimal-risk) review. | The same |
| Agent contrast | Agent outputs only | Not human subjects research | None needed |

If you want the whole application to stay exempt, drop B' for Spring 2027. Paper 2's main test, whether GLP predicts the transfer check beyond artifact quality, can run on the core instruments alone; only Y₆ and Y₇ need B'. Since exempt and expedited review have the same median turnaround (10 business days), the recommendation is to **include B' and let the DHR classify it**.

**FERPA:** coursework, quiz records and LMS logs are education records. Disclosing personally identifiable information from them needs signed, dated written consent that names the records, the purpose and who receives them (34 CFR 99.30). The consent form in [irb/](irb/) carries all three. De-identified records can be released without consent only after all personally identifiable information is removed and a reasonable determination is made that no student is identifiable, "taking into account other reasonably available information" (34 CFR 99.31(b)(1)). In these courses, that other information includes public GitHub repositories. Northeastern's guidance says the Office of the General Counsel must be consulted whenever research uses data that could fall under FERPA; that is step 5.

**Why consent even if part of the study is exempt:** you are the students' instructor, so a request from you carries pressure. Northeastern's guidance, "Recruiting and Enrolling Your Students," lists the remedies, and this plan uses three of them:

1. A third party recruits and collects consent.
2. The instructor does not know who took part, and a third party de-identifies the data.
3. Recruitment happens at the end of the semester, with forms opened only after grades are submitted.

Consent also lets you quote students and write up their projects, which de-identification alone does not safely allow here.

**Why anonymizing is harder in these courses than usual:**
- Student work is posted in public course repositories on GitHub, in folders named by first name and last initial.
- Commit histories carry usernames and emails.
- Sections are small enough that classmates recognize projects.
- A distinctive sentence from a Frictional log can be found with a web search.

The plan in [irb/data-management-plan.md](irb/data-management-plan.md) handles each of these. An honest broker de-identifies the data before you see it, and papers report derived features (charts and statistics) by default. Quotes appear only with consent, and only after a search check.

### Questions for the DHR

Ask these in the pre-submission email, or put them in the application's cover note:

1. Does one application with a retroactive part (secondary use of Fall 2026 records) and a prospective part (Spring 2027) work, or would you like two?
2. Some course records are posted in public GitHub repositories as part of the course. Does that change the analysis for the retroactive part (46.104(d)(4)(i) versus (ii))?
3. The Spring 2027 design counterbalances spaced retrieval and hint types by random assignment, so every student gets spacing on half the concepts and both hint types. Does that take Part B out of exempt category 1? If so, can it be reviewed as expedited within the same application?
4. Is in-class recruitment by a third party in the last week of classes, with forms sealed until grades are submitted, acceptable? Or do you want recruitment strictly after grades, by email?
5. Who may serve as the third party and honest broker, and what training do they need?
6. Which storage service is approved for identifiable student records used in research? If Northeastern's licensed Claude (claude.northeastern.edu) is used to help code de-identified logs, is the "AI Systems Used in Human Subjects Research" form enough?
7. Do you want the instructor's own example folders (the instructor doing the assignments with Claude) listed, or is self-study outside your review?

---

## Next semester: what every course needs

The full checklist and dated calendar are in [courses/README.md](courses/README.md). The instrument specifications are in [courses/instruments.md](courses/instruments.md). In short:

| Instrument | Feeds | Every course | Full set (optional, likely expedited review) |
|---|---|---|---|
| Milestone commits, difficulty rated before term | Y₁, Y₂ | ✓ | ✓ |
| Frictional log, unchanged | Y₅ | ✓ (already in place) | ✓ |
| Confidence rating after every quiz item | Y₄ | ✓ | ✓ |
| Misconception-coded distractors | Y₂ | ✓ | ✓ |
| Near and far transfer item pairs | Y₃ | ✓ | ✓ |
| Delayed, proctored, in-class transfer check (completion credit) | The independent criterion | ✓ | ✓ |
| Counterbalanced spaced retrieval + week-12 retention quiz | Y₆ | | ✓ |
| Randomized partial or full hints | Y₇ | | ✓ |

Every one of these is ordinary good teaching, given to every student. Students who decline the research lose nothing.

Two small changes to the existing course rules:
- Ask students to commit at the end of every working session.
- Ask them to commit with their GitHub no-reply email, so their personal email is not published in a public repository.

---

## The paper: what has to change

The details are in [paper/revision-plan.md](paper/revision-plan.md). The main changes:

1. **Recast the claims as hypotheses**, each with a test. Claim 03 (gaming every trace costs as much as learning) is the most important and the least supported. Test it with agents told to fake human-looking traces. The likely finding is that robustness comes mostly from *where* a trace is collected (proctored, in class), not from combining seven of them.
2. **Fix the validation circularity.** The preprint builds its "confirmed genuine" class from the same components the model scores, and its "borrowed" class from academic integrity cases. Replace both with an independent criterion: the delayed, proctored transfer check. The information gain test then asks whether GLP predicts that check beyond the assignment score.
3. **Cut the unsourced neuroscience.** The "BDNF upregulated 2.8-fold" and "dendritic spine formation increases 37%" figures trace back to one 2026 MDPI review (Gkintoni et al., *Multimodal Technologies and Interaction*). None of the six papers it cites for them measured BDNF or dendritic spines; they are human MRI, EEG and brain-stimulation studies. Remove both numbers. Rebuild Section 3 on desirable difficulties, the testing and spacing effects, storage versus retrieval strength, and fluency illusions.
4. **Add the literature reviewers will expect:** evidence-centered design, stealth assessment, gaming-the-system detection, knowledge tracing, keystroke logging (including recent work detecting non-authentic text from keystrokes), calibration, transfer, AI-detector failure studies, commercial process-capture tools, and learning analytics ethics. Verified references: [paper/references-to-add.md](paper/references-to-add.md).
5. **Tighten the formalism.** Fixes for each problem are in [study/measures.md](study/measures.md).
   - Y₂'s chance level is the density of the adjacency matrix, not 0.
   - Y₃ is defined in two different ways.
   - Y₄_dir is used but never defined.
   - Y₅'s scale is never stated.
   - "Credible interval" names a Bayesian quantity the ensemble does not produce.
6. **"Tier" becomes "facet",** unnumbered, using the current Irreducibly Human names: Pattern & Association, Embodied & Sensorimotor, Social & Personal, Metacognitive & Supervisory, Causal & Counterfactual, Collective & Distributed, and Existential & Wisdom.

---

## Where to submit

Dates checked on 2026-11-22. "Expected" means not yet announced and estimated from the previous year.

| Venue | Fit | Next deadline | Notes |
|---|---|---|---|
| **SIGCSE TS 2028**, Experience Reports and Tools track | **Paper 1 (recommended)** | Expected late June (abstract) and early July 2027 (paper) | 2027 edition: abstracts June 26, papers July 3, 2026; 6 pages plus 1 of references; anonymous review |
| Koli Calling 2027 | Paper 1 alternative | Expected mid-July 2027 | 2026: papers due July 12 (extended to July 19); 10 pages; ACM ICPS |
| EDM 2027 (Adelaide, July 18 to 23) | Paper 1, early option, only if Fall consents arrive by mid-January | Abstracts **February 8**, papers **February 15, 2027** | Fits process-trace mining; tight |
| ITiCSE 2027 (Glasgow, July 12 to 14) | Not recommended | Abstract January 11, paper January 18, 2027 | Too soon for consented Fall data |
| AIED 2027 / L@S 2027 (Adelaide, July 18 to 23) | Not recommended for Paper 1 | AIED papers February 1; L@S papers January 29, 2027 | Too soon |
| ICER 2027 | Paper 2 is too late for it; consider ICER 2028 | Expected late February to early March 2027 | Research track; asks for ethics approval details |
| **LAK28** | **Paper 2 (recommended)** | Expected late September 2027 | LAK27 (deadline September 28, 2026) is publishing full papers in Journal of Learning Analytics special issues as a trial |
| **Journal of Learning Analytics** | Paper 2, or Paper 1 expanded | Open submission system | Open access, no fees, 8,000-word limit for research papers, CC BY 4.0 |
| Computers and Education: Artificial Intelligence | Paper 2 alternative | Open submissions (not verified) | Gold open access; publication fee about USD 2,940 per DOAJ (Elsevier's own page not verified) |

Sources:
- [SIGCSE TS 2027 CFP](https://sigcse-ts.acm.org/2027/files/SIGCSETS-2027-CFP.pdf)
- [ITiCSE 2027](https://iticse.acm.org/2027)
- [Koli Calling 2026 CFP](https://easychair.org/cfp/kolicalling26)
- [EDM 2027](https://educationaldatamining.org/edm2027/important-dates/)
- [AIED 2027](https://www.aied-conference.org/2027/important-dates)
- [L@S 2027](https://learningatscale.hosting.acm.org/las2027/)
- [ICER 2026](https://2026.icer.acm.org/track/icer-2026-papers)
- [LAK27](https://www.solaresearch.org/events/lak/lak27/general-call/)
- [JLA policies](https://learning-analytics.info/index.php/JLA/policies)
- [C&E:AI on DOAJ](https://doaj.org/toc/2666-920X)

---

## Sources for the IRB and calendar facts

- DHR, how to submit: [Get Started](https://dhr.research.northeastern.edu/getstarted/) and [Review types and processes](https://dhr.research.northeastern.edu/wp-content/uploads/2023/08/Review-types-processes-07.15.2023.pdf)
- DHR, training: [CITI requirement](https://dhr.research.northeastern.edu/training)
- DHR, turnaround times: [Fall 2025 newsletter](https://dhr.research.northeastern.edu/fall-2025-irb-newsletter)
- [Policy 505](https://policies.northeastern.edu/policy505), and [the May 2025 change that allows recruiting your own students](https://dhr.research.northeastern.edu/spring-2025-newsletter-special-edition/)
- DHR guidance: [Recruiting and Enrolling Your Students](https://dhr.research.northeastern.edu/wp-content/uploads/2025/05/Recruiting-and-Enrolling-Your-Students.pdf) (third party, end of semester, FERPA and the Office of the General Counsel)
- DHR guidance: [Exemption categories and examples](https://dhr.research.northeastern.edu/wp-content/uploads/2023/05/Exemptions-categories-examples-08.22.2023.pdf) (random assignment is probably not exempt)
- DHR: [AI Systems Used in Human Subjects Research form](https://dhr.research.northeastern.edu/new-form-ai-systems-used-in-human-subjects-research-9-8-2025/)
- Federal rules: [45 CFR 46.104](https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-A/part-46/subpart-A/section-46.104), [34 CFR 99.30](https://www.ecfr.gov/current/title-34/subtitle-A/part-99/subpart-D/section-99.30), [34 CFR 99.31](https://www.ecfr.gov/current/title-34/subtitle-A/part-99/subpart-D/section-99.31)
- [Northeastern 2026–2027 academic calendar](https://registrar.northeastern.edu/wp-content/uploads/sites/9/2026-2027-Academic-Calendar.pdf) (marked "subject to change")

---

## Repository map

| Path | What it is |
|---|---|
| [paper/frictional.md](paper/frictional.md) | The draft: the preprint as published, to be revised in place |
| [paper/revision-plan.md](paper/revision-plan.md) | Section-by-section changes; the claims as hypotheses; Paper 1 outline |
| [paper/references-to-add.md](paper/references-to-add.md) | Verified references for related work and the new Section 3 |
| [irb/application-draft.md](irb/application-draft.md) | Draft answers for the IRB application |
| [irb/consent-form-draft.md](irb/consent-form-draft.md) | Consent wording, prospective and retroactive versions |
| [irb/recruitment-script.md](irb/recruitment-script.md) | What the third party says and posts |
| [irb/data-management-plan.md](irb/data-management-plan.md) | Honest broker, de-identification, storage, and what may be published |
| [courses/README.md](courses/README.md) | Spring 2027 setup checklist and dated calendar |
| [courses/instruments.md](courses/instruments.md) | The eight instruments, and how to build each |
| [study/measures.md](study/measures.md) | Operational definitions of every measure; the information gain test |
| [study/agent-contrast.md](study/agent-contrast.md) | Agents completing the assignments: the contrast and red-team conditions |
| [docs/review-2026-11-22.md](docs/review-2026-11-22.md) | The review this plan is built from |

**Never put student data in this repository.** The `.gitignore` blocks `data/`, `exports/` and `consent/`, but the rule is what protects students, not the file. Keep this repository private.

## Open decisions

- Which courses run in Spring 2027, and whether any section carries the full (randomized) instrument set.
- Who the third party is.
- In-class recruitment in the last week with sealed forms, or email recruitment only after grades (the DHR may prefer one).
- Whether Part A includes terms before Fall 2026 (records from Fall 2025 and Spring 2026 courses exist).
- Whether student work stays in public repositories in Spring 2027. It is a teaching choice, but it is the largest re-identification risk.
- Authorship, affiliation order, and the rights statement for the paper. The Frictional book repository says Bear Brown, LLC; the preprint says the research was conducted through Humanitarians AI. Decide before submission. This repository carries no license.
