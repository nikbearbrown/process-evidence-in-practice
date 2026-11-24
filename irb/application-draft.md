# IRB application: draft answers

> **Status (2026-11-22):** written for the earlier study design, which validated a learning score against a transfer check and used Fall 2026 records. Paper 2 is now a classroom study of the Frictional audit. What changes in this file is listed in [irb-protocol-notes.md](../irb-protocol-notes.md) §11.
>
> **Update (2026-11-23):** the comprehension probe (instrument I-9) added to §4, §5, §8 and §10 by Claude Code (Claude Opus 5.5) for the owner's review. The rest of the file is still the earlier design.

## Executive summary

**What this is:** draft answers to the questions an IRB application for this study will ask, written so they can be pasted into the Department of Human Research (DHR) application form section by section. Northeastern takes applications by email: everything goes to IRBReview@northeastern.edu.

**Why read it:** one application should cover everything the two papers need from students: the retroactive use of past course records and the prospective design for Spring 2027. Writing it once, carefully, is faster than an application now and an amendment in January.

**What it asks for:** a determination with two parts. Part A (past courses, Fall 2026 and earlier) asks for exemption as secondary research use of existing records, 45 CFR 46.104(d)(4)(ii), with consent sought after grades for anything quoted or written up as a case study. Part B (Spring 2027 courses) asks for exemption as research on normal educational practices, 46.104(d)(1), with opt-in consent collected by a third party at the end of the semester. If Part B includes the randomized instruments (spaced retrieval sets and hint versions), the DHR's own guidance says random assignment to instructional strategies "would probably not be exempt", so that part should be flagged and is likely to be reviewed as expedited (minimal risk). Part B also includes an in-class comprehension probe built from each student's own code (I-9), with hints in a fixed order, not randomized. The agent contrast runs involve no people and are described only so the IRB sees the whole study. A human red-team study (people trying to game the measures) is **not** in this application; it would be a later amendment or a separate protocol.

The IRB decides which categories apply, and may decide differently. Where this draft guesses, it says so.

---

## 1. Title

Process traces of learning in courses where students can use generative AI (Frictional)

## 2. Investigator

Nik Bear Brown, Associate Teaching Professor, [department/college], Northeastern University. Human-subjects training: [CITI course and completion date].

Training: CITI "Human Subjects Research, Stage 1 Basic Course" under the Northeastern University affiliation, valid 3 years.

Other personnel: [third party / honest broker: name, role, CITI training]. [Coders for Y₅, if any: names, training; de-identified data only.]

## 3. Purpose and background (plain language)

Generative AI can now produce essays, code and other coursework, so the finished work no longer shows on its own that a student learned. This study asks whether records of the *process* of coursework (when students work, the order of their mistakes, how well their confidence matches their accuracy, what they write in a required reflection log) carry information about learning beyond the finished work. Success is judged against an independent measure: a short, proctored, in-class transfer check near the end of term.

The study aims to publish (a) an experience report on whether such process measures can be computed in ordinary courses and (b) a validation study of whether they predict the transfer check beyond assignment scores.

## 4. Design

**Part A: past courses (retroactive).** Records already created in [list of courses], Fall 2026 [and earlier terms, if included]: FRICTIONAL.md reflection logs, git commit histories of course work, and assignment scores. No new data are collected. Records are used only for students who consent after final grades are submitted; [if the IRB allows] records of non-respondents may be used only in aggregate after de-identification.

**Part B: Spring 2027 courses (prospective).** The courses include, for every student, activities that are established teaching practice: confidence ratings on quiz items, quiz answer choices tied to common misconceptions, near and far transfer items, spaced retrieval quizzes (in some sections, with concept sets counterbalanced between two randomly assigned groups so every student receives spaced practice on half the material), practice problems with hints (randomized partial or full hint), a week-12 in-class retention quiz, and a short in-class, paper, proctored transfer check in the final weeks for completion credit. These are part of the course whether or not a student consents. Research use is limited to consenting students' records.

**Comprehension probe (instrument I-9).** In courses whose projects are written in Python, each student takes a short in-class probe built from their own project, after a project deadline, on a date announced in advance, with no AI and no notes. Part 1 is a sheet of 3 to 5 predict-the-output items (about 3 minutes each) on functions in the student's project that are not in the course starter, showing only each function's signature and docstring; it is collected before part 2 is handed out. Part 2 has one injected-bug item (up to 15 minutes; a partial hint at 5 minutes and a full hint at 10, in that order, for anyone who has not yet fixed it) and one near and one far transfer task (about 10 minutes each). The whole probe takes at most about 50 minutes. One optional re-probe, 4 to 6 weeks later, uses form B: the same functions with new inputs, predict items only, about 10 to 15 minutes. Students rate their confidence before each item. Every student in a section gets the same kinds and number of items, for completion credit only. A probe is never triggered by an audit finding and never used as an integrity check. Answer keys come only from running the student's code in an isolated container, with no credentials and the network off after setup, never on the instructor's own machine. The instructor records one receipt per student per session: item IDs, confidence, times, hint rung and correctness, with no names, answers or code. Probe records are used for research only for consenting students, and only after this protocol is approved.

**Agent contrast (no human subjects).** AI agents complete the same assignments; their outputs are compared with students'. No people are involved.

## 5. Exemption categories requested

**Part B, core instruments: 46.104(d)(1), normal educational practices.** The research takes place in established educational settings (graduate courses at Northeastern) and involves normal educational practices: instructional strategies (retrieval practice, calibration training) and assessment techniques (quizzes with confidence ratings, transfer items, a transfer check). None is likely to adversely affect students' opportunity to learn required content or the assessment of educators who provide instruction. The transfer check carries completion credit only, so no student is graded down for an unannounced item. No student is randomly assigned to anything. The comprehension probe is an assessment technique on the student's own course project; its hints come in a fixed order (partial, then full) for every student who has not yet solved the item, and it carries completion credit only. [Ask the DHR whether a probe built from each student's own code stays within (d)(1).]

**Part B', randomized instruments (only if used): request expedited review if the DHR judges it non-exempt.** In the largest section(s), students are randomly divided into two groups that receive spaced retrieval quizzes and hints on different halves of the material, counterbalanced so that every student receives the same amount of spaced practice and both hint types. The DHR's exemption guidance says random assignment to different instructional strategies would probably not be exempt; the risk is minimal, because no student receives less instruction than another. If the comprehension probe's partial and full hints were instead randomized per student, the probe would belong in this part too.

**Part A: 46.104(d)(4), secondary research use of existing records.** The records exist already, were created for instruction, not for this study, and will be recorded by the honest broker in a way that the identity of the student cannot readily be ascertained; the investigator will not contact students (the third party does, for consent) and will not attempt re-identification. [Some course records are posted in public GitHub repositories, which may bear on (d)(4)(i); this application does not rely on that, and asks for consent for anything quoted or described as a case study.]

## 6. Participants

Graduate students enrolled in the listed courses, 18 or older. Approximate numbers: Part A [about 90 students with logs in Fall 2026 course repositories]; Part B [estimated enrollment by course]. No one is excluded from the course activities; the study includes only those who consent.

## 7. Recruitment and consent

- Recruitment follows the DHR guidance "Recruiting and Enrolling Your Students": a third party recruits and collects consent, the instructor does not know who participates, a third party de-identifies data before analysis, and recruitment takes place at the end of the semester.
- Spring 2027: the third party visits each class in the last week of classes (instructor absent), collects forms, and seals them until final grades are submitted (May 4, 2027); absent students are invited by email after that date. Script: [recruitment-script.md](recruitment-script.md).
- Consent is opt-in, written (or electronic, if approved), with separate options for (1) use of records, (2) quoting log excerpts, (3) a case-study description reviewed by the student before publication. See [consent-form-draft.md](consent-form-draft.md).
- The form includes the elements required for a written FERPA release (the records, the purpose, the parties receiving them).
- The instructor does not learn who consented [at all / until after final grades are submitted].
- Part A: consent is requested by email from the third party after Fall 2026 grades are submitted (December 22, 2026), in early January 2027.
- FERPA: the form includes the elements of 34 CFR 99.30 (records, purpose, recipients). The Office of the General Counsel has been consulted: [date and outcome].

## 8. Risks and how they are reduced

| Risk | Reduction |
|---|---|
| Students feel pressure to take part because the researcher is their instructor | Third-party recruitment and consent; instructor absent; instructor blind to consent status until after grades or permanently |
| Re-identification: public repositories, small classes, distinctive projects, writing style | Honest-broker de-identification; derived features only by default; quotes only with consent and after a search check; case studies only with consent and student review; no statistics for groups under 5 |
| Grades affected by research activities | All activities are course activities for everyone; the transfer check and the comprehension probe are completion credit |
| Data exposure | Restricted-data storage approved by Northeastern; key held by the honest broker and destroyed on a set date; no student data in personal AI accounts |
| The comprehension probe's sheets contain the student's own code, which can identify them in a public repository | Probe specs, sheets, answer keys and bug variants are never exported for research. Only receipts (no names, answers or code) and numbers derived from them are exported, for consenting students, after grades. |
| A probe result is read as a sign of misconduct, or as proof of who wrote the code | Same kinds and number of items for every student in a section, on an announced date; never triggered by an audit finding; never the sole basis for a grade or an integrity action |
| Student code run to compute answer keys damages systems or leaks data | Run only in an isolated container with no credentials and the network off after setup, never on the instructor's machine |

See [data-management-plan.md](data-management-plan.md).

## 9. Benefits

No direct benefit to participants. The study may help instructors evaluate learning without relying on AI detection.

## 10. Data, storage, sharing, retention

As in [data-management-plan.md](data-management-plan.md). Only de-identified data leave Northeastern-approved storage. If any AI model is used on student text (for example to assist coding), it is a Northeastern-licensed service, and the DHR form "AI Systems Used in Human Subjects Research" is attached: [name the tool, or state that none is used].

The comprehension probe's generator uses no AI model. It picks functions, writes items and checks receipts by fixed rules, and every answer key comes from a container run of the student's code, never from a model. An AI agent may draft only the wording of the two transfer tasks. Each draft is labelled with the model's name, and the instructor must approve it before the probe is frozen. Any agent used this way works on student code, so it is a Northeastern-licensed service named on the AI-systems form: [name the tool, or state that none is used].

## 11. Funding and conflicts of interest

[State funding, if any.] The investigator founded Humanitarians AI (a 501(c)(3) nonprofit) and Bear Brown and Company. [State whether either has a financial interest in assessment tools or in the results; ask the conflict-of-interest office if unsure.]

## 12. Not included, to be added later by amendment

- A human red-team study in which participants try to raise their process scores without learning the material. This is not normal educational practice and would need its own review.
- Any course beyond those listed.
