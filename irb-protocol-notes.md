> **Provenance.** Drafted by Claude Code, model Claude Opus 5.5 (`claude-opus-5-5`), on 2026-11-22. Phase 1 deliverable for Paper 2. The comprehension probe (I-9) was added on 2026-11-23 by the same model, after the owner approved adding it to the application (Frictional probe design, decision 9a).
>
> **Human sign-off** (left blank until a human fills it in)
> Name: ____________ Date: ____________ Decision (approved / approved with changes / rejected): ____________ Notes: ____________

> **These are notes for a conversation with Northeastern's IRB office (the Department of Human Research, DHR). They are not legal or regulatory advice.** The DHR decides the review category and what the protocol must contain. The Office of the General Counsel decides FERPA questions.

# IRB protocol notes: Paper 2 classroom study

## Executive summary

**What this is:** the topics the Paper 2 protocol has to address, organized for the DHR: participants, consent, timing, procedures, data handling, FERPA, AI tools, running student code, multi-site reliance, amendments, risks, and RQ6. Each topic gives the design as it now stands and the question to put to the DHR.

**Why read it:** to have a decision by January 13, 2027, the application has to reach IRBReview@northeastern.edu by **December 4, 2026**. The DHR's median turnaround for new exempt and expedited applications is 10 business days. The earlier drafts in [irb/](irb/) were written for a different study (validating a learning score against a transfer check). This file lists what has to change in them.

**What it found:**
- **This is a study with two kinds of participants.**
  - Students, whose work is audited and whose records are analyzed with consent.
  - Instructors and teaching assistants, who produce research data themselves: finding markings, decision logs and time records.

  The teaching assistants work for the investigator, so their consent needs the same third-party protection as the students'.
- **The review category depends on two design choices.** The first is whether review conditions are randomly assigned (DHR guidance: random assignment is "probably not exempt"). The second is whether every student's work is audited by an AI tool as course practice. The recommended two-pass design avoids random assignment.
- **Running student code** (the install test) and **processing student work with an AI tool** both need explicit treatment. Northeastern's DHR has a form for AI systems used in research (added September 8, 2025).
- **A new instrument, the comprehension probe (I-9),** builds an in-class probe from each student's own code. It is teaching use only until the DHR approves a protocol that lists it and the student consents (§4, §5 question 5, §6, §9).

## 1. Participants

| Group | Who | Approximate number | What they contribute | Notes |
|---|---|---|---|---|
| Students | Enrolled in the audited Spring 2027 courses | About 200 (course list to confirm) | Their submissions, git histories, FRICTIONAL.md logs, the audit reports about their work, their grades. Optionally, a post-grade work-style survey (RQ5, RQ6). | Graduate courses; confirm that no one under 18 is enrolled. If someone is, exclude them or follow the DHR's guidance on minors. |
| Instructor-investigator | The author | 1 | Markings, decision logs, time records | Both researcher and participant; mitigation in §9 |
| Teaching assistants | The courses' TAs | To confirm | Independent markings on a sample; possibly their own decision logs and times | Employed and supervised by the investigator: consent through the third party, and participation not tied to employment |
| Other instructors (later) | Northeastern colleagues or other institutions | By amendment | Same as the instructor | See §8 |

## 2. Consent procedure

- **Students:** opt-in; recruited and consented by a third party who neither teaches nor grades the course. Recruitment happens in the last week of classes (April 20 to 23, 2027), with the instructor absent, and forms are sealed until grades are posted. Students who were absent are invited by email after May 4, 2027. This follows the DHR guidance "Recruiting and Enrolling Your Students" (third party; instructor unaware of who participates; end of semester).
- **Separate consent options:**
  1. Use of records.
  2. Quotation of log text.
  3. A case-study description, reviewed by the student before publication.
  4. The optional work-style survey.
- **Instructors and teaching assistants:** written consent through the third party. Teaching assistants are told that participation is not part of their duties or evaluation, and that declining has no effect.
- **What the consent form must now say,** beyond the earlier draft:
  - that each submission was audited by an AI tool as part of the course, if that is the design (open decision 2 in the Paper 2 outline);
  - which tool was used, and that no data went to Irreducibly Human;
  - that audit findings were never the sole basis for a grade or an integrity action.
- **FERPA elements in the student form:** the records, the purpose, and who receives them (34 CFR 99.30). DHR guidance says a signed, IRB-approved consent form usually satisfies FERPA's signed-authorization requirement. The Office of the General Counsel confirms.

## 3. Timing

| When | What | Who knows consent status |
|---|---|---|
| By December 4, 2026 | Application to the DHR; email to the Office of the General Counsel on FERPA | — |
| Before January 13, 2027 | DHR determination; the skill version frozen for the term after passing Paper 1's benchmark; instruments built into the courses | — |
| January 13 to April 25, 2027 | Instruments run; submissions audited (if audits are course practice); instructors and TAs record markings, decision logs and times for all submissions, as part of their grading practice | No one at the course |
| April 20 to 23 | Third-party recruitment visit; forms sealed | Third party only |
| After May 4, 2027 (grades due at 2:00 p.m.) | Forms opened; absentees emailed; honest broker exports and de-identifies consenting students' records; analysis begins | Third party; the instructor only after grades, or never |

The instructor's own markings and logs are recorded during the term for all submissions. Only consenting students' rows are kept for research. Ask the DHR whether rows for non-consenting students must be destroyed, or simply never exported.

## 4. Procedures

- **The audit:** the Frictional skill, at a frozen version, run by the institution-provided AI agent. The DHR form "AI Systems Used in Human Subjects Research" (added September 8, 2025) is likely required. Name the tool. If Northeastern's licensed Claude is used, say so. Confirm with the DHR and Information Technology Services that it is approved for student records.
- **Install tests run student code.** They run in an isolated sandbox: no credentials, network restricted, resource limits, transcript recorded. Student code never runs on the instructor's own machine outside the sandbox. Describe the sandbox in the protocol.
- **Two-pass review** (recommended design): pass 1 without the report, pass 2 with it. Each step is recorded: provisional assessment, time, per-finding marks, relevance, change in assessment.
- **Teaching assistant double-marking:** a random 20 to 30% sample, blind to the instructor's marks.
- **Optional post-grade survey (students):** a few items on work style (offline work, squash merges, prior experience). Only if RQ5 and RQ6 keep it.
- **Optional transfer check:** an in-class, proctored check near the end of term, completion credit only. Only if the secondary analysis is kept.
- **Comprehension probe (I-9):** an in-class probe with no AI and no notes, built by Frictional from each student's own Python project. It has predict-the-output items, one injected-bug item with a hint ladder that is not randomized (partial hint at 5 minutes, full at 10), and one near and one far transfer task the instructor writes. Keys come from running the student's code in the install test's container, with the network off after setup. Every student in a section takes it, on an announced date, for completion credit; it is never triggered by an audit finding. An optional re-probe 4 to 6 weeks later. If an AI agent drafts the transfer wording from student code, name it on the AI-systems form. See [courses/instruments.md](courses/instruments.md) I-9.

## 5. Review category: questions for the DHR

1. With the two-pass design, there is no random assignment. Does the student side fit exemption category 1, normal educational practices (45 CFR 46.104(d)(1)), given that an AI audit of submissions is a new practice in these courses?
2. The instructor and teaching assistant data (markings, decision logs, time) come from people, not students. Which category covers them, and do they need their own consent form?
3. If random assignment of submissions to review conditions is used instead (Paper 2 open decision 3, option b), the DHR's exemption guidance says it would "probably not be exempt". Can it be reviewed as expedited within the same application?
4. Is in-class recruitment in the last week of classes, with forms sealed until grades, acceptable, or should recruitment be email-only after grades?
5. The comprehension probe (I-9) gives each student a bug item built from their own code, with a hint ladder that is not randomized: anyone who has not fixed the bug sees the partial hint at 5 minutes and the full hint at 10. Does that stay within normal educational practice (46.104(d)(1))? If partial against full hints were instead randomized per student, as in I-7, would that change the category, as random assignment does for I-6 and I-7?

## 6. Data handling

- **Honest broker:** the third party holds the consent forms and the code key. They export consenting students' records after grades and replace identifiers with codes, before the investigator sees any research data. See [irb/data-management-plan.md](irb/data-management-plan.md).
- **What is identifying here:**
  - Course repositories may be public, with folders named by first name and last initial.
  - Commit histories carry usernames and emails.
  - Audit reports quote file paths and log text.
  - Small classes make projects recognizable.
- **Reports are records too:** the audit reports about each student's work are research data and education records. Store and de-identify them like the submissions.
- **Probe files (I-9):** specs, student sheets, instructor keys and bug variants contain the student's code, so they identify students whose repositories are public. They stay in the course, outside every repository, and are never exported for research. The honest broker exports receipts (item IDs, confidence, times, hint rung, correctness; no names, answers or code) and the evidence packets derived from them, for consenting students only, after grades. Receipts never record accommodation status.
- **Storage:** a Northeastern-approved location for restricted student data. Ask the DHR or Information Technology Services which one.
- **Publication:** aggregate statistics and charts by default; quotes only with consent and after a web-search check; no statistics for groups below a minimum size.
- **Retention and destruction:** per DHR requirements; destroy the key on a set date.
- **Nothing goes to Irreducibly Human.** Instructor feedback on the website uses enumerated values only and carries no student data.

## 7. FERPA

- Student work, audit reports about it, and grades are education records.
- The Office of the General Counsel must be consulted whenever research uses data that could fall under FERPA (DHR guidance). Ask:
  - Is the signed consent form enough?
  - Does auditing every student's work with an AI tool as course practice raise a separate FERPA question about disclosure to the tool's provider, under the university's contract with that provider?
- De-identified release without consent requires removing all personally identifiable information, with a reasonable determination that no student is identifiable "taking into account other reasonably available information" (34 CFR 99.31(b)(1)). Public repositories are that other information.

## 8. Multi-site reliance and amendments

- **Other Northeastern instructors** join by amendment to this protocol: they are added as personnel, their courses are listed, and they complete CITI training (DHR requires the CITI "Human Subjects Research, Stage 1 Basic Course" under the Northeastern affiliation, valid 3 years).
- **Instructors at other institutions** need IRB coverage. Either their own IRB reviews their site, or their institution signs a reliance agreement with Northeastern as IRB of record. Ask the DHR:
  - How long does a SMART IRB reliance take for a non-exempt protocol?
  - If the protocol is exempt, what should external instructors give their own IRBs (a copy of the Northeastern determination and protocol)?

  Checked 2026-11-22 on the DHR's [IRB reliance page](https://dhr.research.northeastern.edu/irb-reliance/):
  - "For non-exempt research, NU will serve as the IRB of record for US based institutions which have a FWA on file."
  - Northeastern will also cede review to a U.S. IRB of record.
  - "We encourage investigators to use SMART IRB whenever possible." Northeastern is on SMART IRB's participating-institutions list. Institutional agreements (IAAs) and individual investigator agreements (IIAs) are available; IIAs cover collaborators at institutions without an FWA.
  - **"The NU IRB does not enter into reliance agreements or establish IIAs for exempt research."** So if Paper 2 is determined exempt, every external site needs its own IRB determination. If it is non-exempt (for example, expedited because of random assignment), external sites can rely on Northeastern.
  - Northeastern's FWA number, per the DHR page: 00004630.
- **Amendment path for adding courses or terms:** DHR's newsletter reports a median of 3 business days for modifications.
- **Not covered by this protocol:** a human red-team study, in which people try to game the audit; Fall 2026 or earlier records (retroactive use), unless the human decides to add them.

## 9. Risks and mitigations

| Risk | Mitigation |
|---|---|
| Students feel pressure to consent to their instructor | Third party; end of term; forms sealed until grades; instructor blind to consent until grades are posted, or permanently |
| Teaching assistants feel pressure to participate for their supervisor | Third-party consent; participation not part of duties or evaluation |
| An audit finding is wrong and harms a student's grade or standing | Findings are observations with alternative explanations, never verdicts. The course policy says findings are never the sole basis for a grade or integrity action. The two-pass design records every change, so harms are visible in the data. |
| Re-identification from public repositories, reports or quotes | Honest broker; derived statistics by default; quotes only with consent and a search check; minimum group size |
| Student code run in the install test or the probe's key run damages systems or leaks data | Isolated sandbox; no credentials; restricted network |
| A probe result is read as a sign of misconduct, or as proof of who wrote the code | Same kinds and number of items for every student in a section, on an announced date; never triggered by an audit finding; completion credit; never the sole basis for a grade or integrity action. The tool says "changed from the starter", not "written by the student". |
| Probe files identify students (they contain their code), or probe timing reveals an accommodation | Specs and sheets never exported; receipts hold no names, answers or code and never record accommodation status; extended intervals left out of Y₁ |
| Student work processed by an AI provider | Institution-provided tool under its contract; the DHR AI form; stated in the syllabus and consent form |
| Investigator bias (researcher and participant) | Blind independent TA marking; pre-registered marking guide; separate analysis of instructor and TA markings |
| RQ6 groups expose sensitive characteristics | Method only as approved; no institutional sensitive data unless the DHR and the Office of the General Counsel approve; minimum group size |

## 10. RQ6: method options for the DHR

RQ6 asks whether false positives cluster by work style or student circumstance. Any method needs DHR approval. Options, from least to most sensitive:
1. Work-style groups derived from the audit itself (for example, histories with squash merges or bulk pushes). No new data is collected.
2. An optional post-grade student survey with a few work-style items (offline work, prior experience, whether they worked on a shared or university machine), covered by its own consent box.
3. Institutional records about student circumstances (for example, international status or accommodations). Sensitive; needs FERPA review and is likely not approved. Not recommended.

## 11. What changes in the existing drafts in [irb/](irb/)

| Draft | Written for | Change needed |
|---|---|---|
| [irb/application-draft.md](irb/application-draft.md) | Validating a learning score against a transfer check; Part A retroactive Fall 2026 data | Replace the purpose with Paper 2's research questions. Add instructor and TA participants. Add the AI tool and the sandbox. Add the two-pass review procedure. Remove Part A unless retroactive use is kept. Keep the transfer check only as the optional secondary analysis. |
| [irb/consent-form-draft.md](irb/consent-form-draft.md) | Students only | Add: the audit as course practice and the tool used; the no-verdict policy; the survey box. Add a separate instructor and TA consent form. |
| [irb/recruitment-script.md](irb/recruitment-script.md) | End-of-term student recruitment | Still valid. Add a TA recruitment script. |
| [irb/data-management-plan.md](irb/data-management-plan.md) | Honest broker, de-identification | Add the audit reports as records; add markings, decision logs and time records. |
| [courses/](courses/) | GLP instruments (Y₁ to Y₇, transfer check) | Keep the commit, README, process-log and push-record instruments. Keep quiz instruments and the transfer check only if the secondary analysis is kept. Add the two-pass review logging. |
| Comprehension probe (I-9), across the files above | New: Frictional probe design approved 2026-11-23 (decision 9a) | Drafted 2026-11-23 for review: I-9 in [courses/instruments.md](courses/instruments.md), probe notes in [study/measures.md](study/measures.md), lines in the consent form and data plan, and §4, §5, §6 and §9 here. Also drafted 2026-11-23: I-9 in [irb/application-draft.md](irb/application-draft.md) (§4 design, §5 categories, §8 risks, §10 AI form) and placeholder probe dates in the calendar in [courses/README.md](courses/README.md). Still to do: real project deadlines, then real probe dates. |
