> **Provenance.** Drafted by Claude Code, model Claude Opus 5.5 (`claude-opus-5-5`), on 2026-11-22. Phase 1 deliverable: outline of Paper 2. Not a draft of the paper.
>
> **Human sign-off** (left blank until a human fills it in)
> Name: ____________ Date: ____________ Decision (approved / approved with changes / rejected): ____________ Notes: ____________

# Paper 2 outline: classroom use under IRB approval

## Executive summary

**What this is:** a section-by-section outline of Paper 2, the classroom study. For each section it gives the claims and the evidence each claim needs. It also covers title options, research questions, study design, figures, metrics, threats to validity, related work (with verification status), candidate venues, and numbered open decisions.

**Why read it:** Paper 2 asks whether audit findings help instructors assess real student work, and at what cost. It depends on things that must be settled **before Spring 2027 starts on January 13**:
- the IRB application, submitted by December 4, 2026, to get a decision before term;
- the course instruments, in place from the first day;
- a decision about how instructors review work with and without reports;
- a version of the Frictional skill that has passed Paper 1's synthetic benchmark before it touches any student work.

**What it decides and leaves open:**
- **Decided by the brief:** about 200 students in the author's Spring 2027 courses; opt-in consent collected by a third party; the instructor blind to consent until grades are posted, and analysis only after that; students and instructors both as participants; teaching assistants marking findings independently to check the instructor's markings; other institutions joining through their own IRB or a reliance agreement.
- **Recommended here:** a two-pass review design. The instructor assesses each submission without the report, then with it, and records any change. This measures decision impact and added review time without randomly assigning students to different grading conditions. That keeps the study closer to exempt and avoids grading some students differently from others.
- **Left for you:** decisions 1 to 14 below. They include whether every student's work is audited as course practice, how review time is compared, and how RQ6 (false positives by work style or circumstance) is studied, if at all.

The earlier IRB drafts in [irb/](irb/) and the course setup in [courses/](courses/) were written for the preprint's validation design. [irb-protocol-notes.md](irb-protocol-notes.md) lists what changes.

## Title options

1. **Process Evidence in Practice: A Classroom Study of Agent-Run Audits for Assessment** (working title)
2. Frictional in the Classroom: How Instructors Use Evidence of How Student Work Was Made
3. Do Audit Findings Change Assessment? A Classroom Study of Artifact and Process Evidence
4. Precision, Decision Impact and Cost of Agent-Run Audits in Assessment: A Classroom Study
5. What Instructors Do With Evidence of How Work Was Made

## Contribution statement

When generative AI can produce coursework, instructors need evidence of how work was made, but no study has measured whether such evidence helps them assess real student work. In a study approved by the IRB, across [N] courses and about 200 students in Spring 2027, instructors and teaching assistants reviewed submissions alongside reports from Frictional. Frictional is an agent-run audit that reports artifact and process evidence as neutral observations, with alternative explanations and no verdicts. We measure:
- the precision of each dimension's findings on real work, as marked independently by instructors and teaching assistants;
- how often findings changed an instructor's assessment;
- what the reports added to review time;
- which dimensions instructors kept and how relevant they rated them;
- how often known confounds (squash merges, offline work, prior expertise) occurred, and whether reports handled them;
- [if approved] whether inaccurate findings clustered by work style.

Consent was opt-in and collected by a third party, and the instructor learned who took part only after grades were posted. The protocol is built so that other instructors can join through amendments.

## Research questions

- **P2-RQ1:** What is each dimension's finding precision on real work, as marked by instructors during review?
- **P2-RQ2:** How often do findings change an instructor's assessment (decision impact)?
- **P2-RQ3:** How does review time compare with and without the audit report?
- **P2-RQ4:** Which dimensions do instructors enable in different fields and course levels, and how do they rate relevance?
- **P2-RQ5:** How often do confounds (squash merges, offline work, prior expertise) occur in real work, and does the report handle them?
- **P2-RQ6:** Do false positives cluster by work style or student circumstance? *(Any method for this question must be approved by the IRB.)*
- **Optional secondary analysis (from the preprint):** do process findings predict performance on a delayed, proctored, unannounced transfer assessment, beyond what artifact quality predicts?

## Study design

| Element | Design | Status |
|---|---|---|
| Setting | The author's Spring 2027 courses (January 13 to April 25, 2027; grades due May 4). Course list to confirm. | Course list not found |
| Participants: students | About 200 enrolled students whose submissions are audited. Opt-in for research use of their records. | Brief |
| Participants: instructors | The author, the courses' teaching assistants and, by amendment, other instructors. Each provides finding markings, decision logs and time records. Separate consent, collected by the third party; for teaching assistants, participation is not tied to their employment or evaluation. | Brief plus Claude's addition (TA consent) |
| Instruments from day one | Commit at the end of each working session; commits use GitHub no-reply addresses; a README with set sections; the FRICTIONAL.md process log (already in the courses); a push record (CI on push, or instructor snapshots at set times); optional starter instruments (confidence ratings, transfer items) if the secondary analysis is kept | [courses/README.md](courses/README.md), to revise |
| The audit | Frictional, at a version frozen for the term and benchmarked in Paper 1, run by the instructor's institution-provided AI agent on each audited assignment. All dimensions on; instructors hide what they do not want, and hidden dimensions stay listed. Install tests run in an isolated sandbox. | To build |
| Review procedure (recommended: two-pass) | For each submission: (1) assess without the report and record the provisional assessment and time; (2) open the report; for each finding, mark accurate, inaccurate or can't tell, and rate relevance from 1 to 5; record whether the assessment changed, how, and the added time. | Open decision 3 |
| Independent marking | A teaching assistant marks the findings on a random sample of 20 to 30% of submissions, blind to the instructor's markings; agreement is reported. | Brief (mitigation) |
| Consent timing | Third party, last week of classes; forms sealed until grades are posted; absentees invited by email after grades. Research analysis only after grades are posted. | Brief; DHR guidance |
| Analysis | Consenting students' records only, de-identified by an honest broker, after May 4, 2027 | Brief |

## Section-by-section outline

Status key: **have**, **to collect** (the study must produce it), **to verify** (a source exists but is not yet confirmed), **depends on Paper 1**.

### 1. Introduction

| Claim | Evidence needed | Status |
|---|---|---|
| Generative AI weakens the inference from an artifact to the process that produced it. | Decoupling argument (preprint); detector failure studies (Weber-Wulff et al. 2023; Liang et al. 2023) | have |
| Tools that judge AI use are unreliable and shift judgment away from instructors. A report of evidence keeps the judgment with the instructor. | Detector studies; ethics literature (Slade and Prinsloo 2013); preprint §5.3 | have |
| Synthetic evaluation (Paper 1) shows what the auditor can detect, not whether it helps on real work. | Paper 1 | depends on Paper 1 |
| Contributions: the first classroom measurement of precision, decision impact and cost for agent-run audits of student work; a multi-site-ready protocol. | The study | to collect |

### 2. Related work

| Claim | Evidence needed | Status |
|---|---|---|
| Process evidence and its use for assessment (evidence-centered design, stealth assessment, gaming detection, keystroke-based detection) | References verified for Paper 1 | have |
| Instructors' use of learning-analytics information in practice: what they look at, and what changes their decisions | Literature on teacher or instructor use of analytics dashboards | UNVERIFIED (to identify) |
| People can over-rely on automated advice (automation bias), which matters when a report sits beside a grading decision | Automation-bias literature | UNVERIFIED (to identify) |
| Learning-analytics ethics, consent and surveillance concerns | Slade and Prinsloo (2013) | have |
| Commit-history mining in computing education | As in Paper 1 | have (verified) |

### 3. The tool, briefly

| Claim | Evidence needed | Status |
|---|---|---|
| The audited version and its benchmark results | Paper 1 results for the frozen version | depends on Paper 1 |
| Reports contain observations with alternative explanations, no verdicts; facts and interpretations are separated; each finding has its source. | Paper 1 design | depends on Paper 1 |

### 4. Method

| Claim | Evidence needed | Status |
|---|---|---|
| The study was approved or determined exempt by Northeastern's IRB, with the protocol number. | IRB letter | to collect |
| Consent was opt-in and collected by a third party; the instructor learned who consented only after grades; analysis followed grades. | Consent records held by the honest broker; dates | to collect |
| Participants: N students consented of M enrolled; K instructors and teaching assistants | Counts | to collect |
| Instruments were in place from the first day of class. | Course log with dates (`courses/spring-2027-log.md`) | to collect |
| The marking guide defined accurate, inaccurate and can't tell before marking began. | Marking guide, dated | to collect |
| The teaching assistants' independent markings were blind to the instructor's. | Procedure record | to collect |

### 5. Results

| Claim | Evidence needed | Status |
|---|---|---|
| RQ1: precision per dimension, by marker type (instructor, teaching assistant), with confidence intervals and agreement | Markings | to collect |
| RQ2: share of submissions where the assessment changed after the report, and the direction and kind of change | Two-pass decision logs | to collect |
| RQ3: time for pass 1 versus time added by pass 2 (or a comparison between conditions, under the alternative design) | Time records | to collect |
| RQ4: rates at which each dimension was hidden or kept, and relevance ratings, by course field (CIP code) and level | Configuration logs; ratings | to collect |
| RQ5: frequency of each confound in real work and whether the report offered the right alternative explanations | Markings; optional student survey on work style | to collect |
| RQ6: false-positive rates by work-style group (method per IRB approval) | Depends on the approved method | to collect, if approved |
| Secondary: whether process findings add prediction of the transfer check beyond artifact quality | Transfer check scores; findings; artifact scores | to collect, if kept |

### 6. Discussion

| Claim | Evidence needed | Status |
|---|---|---|
| Which dimensions are precise enough on real work to be useful, and which are not | RQ1 and RQ4 | to collect |
| Whether synthetic detection (Paper 1) carried over to real work: the coupling question | Paper 1 versus RQ1 per dimension | to collect |
| Whether the report changed assessments, in which direction, and whether any change looked like over-reliance | RQ2; decision-log text | to collect |
| What a second institution would need to join | The protocol and reliance experience | to collect |

### 7. Ethics and limitations

| Claim | Evidence needed | Status |
|---|---|---|
| Audit findings were never the sole basis for any grade or academic-integrity action. | Course policy text; decision logs | to collect (policy to write) |
| Student work was processed only by the institution-provided AI tool, under institutional policy; nothing went to Irreducibly Human. | Tool configuration; the DHR "AI Systems" form | to collect |
| Single institution, graduate courses, an instructor-researcher, and self-selected consenters limit generalization. | — | to state |

## Planned figures and tables

| # | Kind | Content |
|---|---|---|
| T1 | Table | Courses, fields (CIP), levels, enrollment, consent rates, assignments audited |
| F1 | Figure | The two-pass review procedure and what is recorded at each step |
| T2 | Table | RQ1: precision per dimension (instructor and teaching assistant markings), with agreement |
| F2 | Figure | RQ2: assessment changes after the report, by dimension that prompted them |
| F3 | Figure | RQ3: review time, pass 1 and added pass-2 time, per submission |
| T3 | Table | RQ4: dimensions kept or hidden, and mean relevance, by field and level |
| T4 | Table | RQ5: confound frequencies and whether the report handled them |
| T5 | Table | RQ6 (if approved): false-positive rates by work-style group |
| T6 | Table | Paper 1 synthetic detection compared with Paper 2 real precision, per dimension |

## Evaluation plan and metrics

- **Precision (RQ1):** accurate ÷ (accurate + inaccurate) per dimension, with "can't tell" reported separately. Wilson 95% intervals. Cohen's kappa between instructor and teaching assistant on the double-marked sample.
- **Decision impact (RQ2):** proportion of submissions where the assessment changed between passes, with the change categorized (grade change, feedback change, follow-up conversation). Pre-specify what counts as a change.
- **Review time (RQ3):** in the two-pass design, the median pass-1 time and the median added pass-2 time, timed by a tool, not self-estimated. Under the randomized alternative, the difference in median time between conditions.
- **Relevance and configuration (RQ4):** proportion of instructors hiding each dimension; mean relevance (1 to 5); both by CIP code and course level.
- **Confounds (RQ5):** frequency per 100 submissions; proportion where the report listed the confound as an alternative explanation.
- **RQ6:** false-positive rate per group, with intervals, only under an IRB-approved method and only for groups of at least a pre-specified minimum size.
- **Secondary:** incremental R² of process findings over artifact score in predicting the transfer check, pre-registered.
- **Pre-registration:** OSF, before any research data are opened (that is, before May 4, 2027).

## Threats to validity

| Threat | Kind | Mitigation |
|---|---|---|
| The instructor is researcher and participant, and may mark findings to favor the tool. | Internal | Teaching assistants' independent blind marking with agreement reported; a pre-registered marking guide; analysis of instructor markings and TA markings separately |
| Two-pass design: anchoring on the first assessment; order effects | Internal | Report it; optionally randomize pass order for a subset (with the IRB implication) |
| Students who consent may differ from those who do not. | External | Report consent rates per course; compare non-identifying aggregates (for example, the share of submissions with any finding) between consenters and all submissions, if the IRB allows |
| Students behave differently knowing their process is audited. | Construct | The audit is part of the course for everyone, so this is the real-world condition. State it. |
| One institution, graduate courses, one instructor's assignments | External | Multi-site amendments; report course details |
| Tool or model version drift during the term | Reliability | Freeze the skill version for the term; record the model version on every report |
| Self-reported time | Measurement | Use a timer, not estimates |
| Confounds that cannot be known from the repository (prior expertise) | Construct | Optional post-grade student survey, if approved |

## Related-work map

Status as in Paper 1: **verified** (checked 2026-11-22), **verifying**, **UNVERIFIED**.

| Area | Reference | Status |
|---|---|---|
| Evidence-centered design | Mislevy, Steinberg and Almond (2003), doi:10.1207/S15366359MEA0101_02 | verified |
| Gaming detection; knowledge tracing; stealth assessment | Baker et al. (2004); Corbett and Anderson (1994 or 1995); Shute (2011) | verified |
| Keystroke-based detection of non-authentic text | Jiang et al. (2024); Deane et al. (2025); Crossley et al. (2024) | verified |
| Detector unreliability and bias | Weber-Wulff et al. (2023); Liang et al. (2023) | verified |
| Learning-analytics ethics | Slade and Prinsloo (2013) | verified |
| Performance versus learning; desirable difficulties | Bjork and Bjork (1992, 2011); Bjork, Dunlosky and Kornell (2013) | verified |
| Transfer (secondary analysis) | Barnett and Ceci (2002), doi:10.1037/0033-2909.128.4.612 | verified |
| Commit-history mining in computing education | Mierle et al. (2005); Edwards et al. (2009); Karakaš and Helić (2024); Song, Leinonen and Giacaman (2026); Gedeon and Giacaman (2026). Full details in the Paper 1 outline. | verified |
| Instructor use of learning-analytics dashboards | — | UNVERIFIED (to identify) |
| Automation bias in decision support | — | UNVERIFIED (to identify) |
| Multi-site IRB reliance | Northeastern DHR, [IRB reliance](https://dhr.research.northeastern.edu/irb-reliance/); SMART IRB participating institutions list (Northeastern is listed) | verified 2026-11-22 |
| LLM grading reproducibility | Jukiewicz (2024), *Thinking Skills and Creativity* 52, 101522, doi:10.1016/j.tsc.2024.101522 | verified |

## Candidate venues

All checked on **2026-11-22**. Constraint: only venues where Northeastern University Library fully covers the APC, or that charge authors nothing. Coverage is from the library's open-access page (marked "Updated 11/17/2026"; [NU Library OA](https://library.northeastern.edu/resource_discovery/open-access-publishing/)) and Northeastern's [SciFree checker](https://search.scifree.se/northeastern) (data last updated July 28, 2026). Both require the Northeastern author to be the corresponding author.

| Venue | Fees for a Northeastern corresponding author | Length and format | Review | Deadline | Notes and sources |
|---|---|---|---|---|---|
| **LAK28** (Learning Analytics and Knowledge) | LAK27 full papers are published in the Journal of Learning Analytics, which charges no fees. LAK28's publication route is not announced. | LAK27: full papers 10 to 14 pages, short 6 to 8, in JLA format including references | Double-blind with rebuttal | **Not announced.** LAK27 was abstract September 21, paper September 28, 2026, so expect late September 2027 (estimated) | Publishing in JLA is explicitly a "trial" for LAK27; SoLAR will decide whether to continue. [LAK27 call](https://www.solaresearch.org/events/lak/lak27/general-call/); [proceedings update](https://www.solaresearch.org/events/lak/lak27/proceedings-update/) |
| **Journal of Learning Analytics** | None: "does not charge authors submission or processing charges" | Research papers up to 8,000 words including the abstract; CC BY 4.0 | Double-blind | Rolling | [JLA FAQ](https://learning-analytics.info/index.php/JLA/faq); [submissions](https://learning-analytics.info/index.php/JLA/about/submissions). Not listed in DOAJ. |
| **ACM Transactions on Computing Education (TOCE)** | $0 through ACM Open (Northeastern is a participant; ACM APCs "fully covered") | No page or word limit; most 15 to 25 journal pages | Double-anonymous; monthly cut-off | Rolling. **Review tokens required since November 1, 2026.** | Research articles fit; experience reports are desk-rejected. [Author guidelines](https://dl.acm.org/journal/toce/author-guidelines) |
| **British Journal of Educational Technology** (Wiley) | Covered: hybrid, "Included in Publisher Agreement" (SciFree); Wiley APCs fully covered, no cap stated. List APC $4,680. | 5,000 to 6,000 words excluding references, abstract, practitioner notes and appendices (under 4,000 is desk-rejected); structured Practitioner Notes required; APA | Double-blind | Rolling | [BJET for authors](https://bera-journals.onlinelibrary.wiley.com/hub/journal/14678535/forauthors.html) |
| **Journal of Computer Assisted Learning** (Wiley) | Covered: hybrid, included (SciFree) | **UNVERIFIED** (Wiley site blocked the check) | **UNVERIFIED** | Rolling (UNVERIFIED) | Check the word limit before choosing it |
| **Journal of Educational Computing Research** (Sage) | Covered: hybrid, included (SciFree); "no fees payable to submit or publish"; optional Sage Choice open access (amount UNVERIFIED), which the library covers for Sage hybrid journals | Up to 10,000 words including references; APA 7 | Double-anonymized | Rolling | Read from a Sage-hosted mirror of the guidelines: [JECR instructions](https://sage.cnpereading.com/storage/ext/submission-guidelines/page/author-instructions_JEC.html) |
| ~~International Journal of AI in Education~~ | **Not recommended.** It moved from Springer to Elsevier on January 1, 2026. It is not in Northeastern's SciFree. Northeastern's Elsevier agreement covers "Core-Hybrid" journals only and is capped at 29 APCs for 2026. Coverage: UNVERIFIED and probably not covered. | UNVERIFIED | UNVERIFIED | — | [Springer journal page](https://link.springer.com/journal/40593) says the journal "will be published by Elsevier" |

Deprioritized, as the brief says: Taylor & Francis (5 APCs for all of Northeastern in 2026) and Elsevier (29).

## Open decisions

1. **Title.** Options above.
2. **Is every student's work audited as course practice, or only consenting students' work, after grades?** (a) Every submission is audited during the term as part of grading practice, and only consenting students' records are analyzed afterwards. This is what RQ2 and RQ3 need, but it means an AI tool processes every student's work, so the syllabus must say so and institutional AI policy applies. (b) Audits run only after grades, only on consenting students. Students carry no risk, but RQ2 and RQ3 (decision impact, review time during grading) cannot be measured.
3. **Review-time and decision-impact design.** (a) Two-pass within each submission (recommended): no student is graded under a different condition, and RQ2 is measured directly; RQ3 measures added time, not time saved. (b) Random assignment of submissions to with-report or without-report review: measures time saved, but DHR guidance says random assignment is probably not exempt, and students would be assessed under different conditions. (c) By assignment: some assignments reviewed without reports, others with them. No random assignment, but confounded with the assignment.
4. **Which courses and assignments are audited**, and whether the 200-student target holds once the Spring 2027 course list is confirmed.
5. **Teaching assistant roles.** How many mark independently, what share they double-mark, and how their consent is kept separate from their employment.
6. **RQ6 method.** (a) Work-style groups from the audit itself plus an optional post-grade student survey (offline work, squash merges, prior experience). (b) Add institutional data (for example, international status or accommodations). This is sensitive, needs FERPA review, and is likely to be refused. (c) Drop RQ6 from Paper 2. The brief requires IRB approval for any method.
7. **Course policy on audit findings and academic integrity.** Proposed: findings are never the sole basis for a grade or an integrity referral; any concern follows the university's integrity process with human review. Needs your wording and possibly the dean's office.
8. **Push-timeline evidence.** CI on push, instructor snapshots, or none (see Paper 1's benchmark open decision 4).
9. **Optional secondary analysis (transfer check).** Keep it, which requires the in-class transfer check and possibly the core quiz instruments, or drop it to simplify the course setup.
10. **Pre-registration timing and venue.** OSF before May 4, 2027.
11. **Multi-site.** Recruit other instructors for Spring 2027 (amendment before January), or for a later term. Northeastern serves as IRB of record only for **non-exempt** research at U.S. institutions with an FWA, and "does not enter into reliance agreements or establish IIAs for exempt research." If Paper 2 is exempt, each external site needs its own IRB determination. If it is non-exempt (for example, expedited), external sites can rely on Northeastern, preferably through SMART IRB.
12. **Retroactive data.** The brief limits Paper 2 to next semester's data. The earlier plan also asked to use Fall 2026 records. Confirm that they are out.
13. **Venue.**
    - (a) LAK28, expected late September 2027. It fits the learning-analytics audience, but its publication route after the JLA trial is not announced.
    - (b) The Journal of Learning Analytics directly: free, rolling, 8,000 words.
    - (c) TOCE: free through ACM Open and no length limit, but needs review tokens.
    - (d) BJET: covered by the library, 5,000 to 6,000 words, practitioner notes.
    - (e) JECR: covered by the library, 10,000 words.

    IJAIED is out (now Elsevier, probably not covered). Tradeoff: conference visibility and speed against journal length and certainty.
14. **Authorship**, including any co-investigators from other sites.
