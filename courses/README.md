# Setting up next semester's courses

> **Status (2026-11-22):** written for the earlier study design, which validated a learning score against a transfer check and used Fall 2026 records. Paper 2 is now a classroom study of the Frictional audit. What changes in this file is listed in [irb-protocol-notes.md](../irb-protocol-notes.md) §11.

## Executive summary

**What this is:** the checklist for building the Frictional instruments into every course taught in Spring 2027, with a week-by-week calendar for the term.

**Why read it:** the validation paper (Paper 2) depends entirely on data that only exists if these instruments are in place before the first class. The IRB application describes this design, so build what the application says, and change neither without the other.

**What it decides:**
- **Every course gets the core set:** milestone commits, the Frictional log as now, confidence ratings on quizzes, misconception-coded distractors, near and far transfer items, and the in-class transfer check near the end of term. Most of this is a few extra questions per quiz.
- **One or two courses may get the full set**, adding counterbalanced spaced retrieval and randomized hints. Pick the largest sections: the information gain test needs students, and 20-student sections are too small to carry it alone. The full set randomly assigns students, which probably moves the IRB application from exempt to expedited review; it is optional.
- Nothing here is research-only. Every instrument is part of the course for every student; the research question is only whether consenting students' records may be used.

The instruments themselves are specified in [instruments.md](instruments.md).

## Which courses

The Spring 2027 roster was not found in the local files. The table lists the Fall 2026 courses that already run the Frictional log; confirm which run in Spring 2027 and fill in the last two columns.

| Course | Fall 2026: Frictional log in place | Fall 2026 student folders with logs (count only) | Spring 2027? | Core or full set |
|---|---|---|---|---|
| INFO 7375 Prompt Engineering for Generative AI | Yes | 53 folders, 120 FRICTIONAL.md files | [confirm] | [full if largest] |
| INFO 7375 Computational Skepticism for AI | Yes | 20 folders | [confirm] | |
| INFO 7375 Irreducibly Human | Yes | none in repo yet | [confirm] | |
| INFO 7375 Branding and AI | Yes | 2 folders | [confirm] | |
| INFO 7375 Conducting AI | Yes (private repo) | none in repo yet | [confirm] | |
| CSYE 7270 Building Virtual Environments | Yes | 20 folders, 29 FRICTIONAL.md files | [confirm] | |
| INFO 6205 Algorithms | Pilot drafted (one notebook, Nov 2026) | n/a | [confirm] | |

The counts are of folders and files only; no student work was opened to build this table.

## Before the first day of class (every course)

1. **Item bank** (private, in this repo, never in a public course repo):
   - [ ] List the course's core concepts; mark the ones taught in weeks 2 to 6 (the transfer check targets these).
   - [ ] For each core concept: one near-transfer and one far-transfer item, with a note on what makes the far item far.
   - [ ] Every quiz distractor tagged with a misconception code; the adjacency map of misconceptions, checked by a second person.
   - [ ] Every assignment split into 3 or 4 milestones, each rated 1 to 5 for difficulty, dated.
2. **Canvas:**
   - [ ] A 0-point confidence item after every scored quiz item (0, 25, 50, 75, 100%).
   - [ ] The in-class transfer check (paper) written and set aside for weeks 13 to 14; completion credit only.
   - [ ] On a test course: export a quiz report and confirm the confidence columns come out per item.
3. **Course repository:**
   - [ ] One line added to `prerequisites/frictional.md`: commit at the end of every working session.
   - [ ] One line added to the GitHub setup instructions: use the GitHub no-reply email for commits.
   - [ ] Milestone names in each assignment's instructions.
4. **Syllabus:**
   - [ ] Describe the activities as part of the course (they are): confidence ratings, review quizzes, hinted practice, the in-class check. No research language is needed there.
   - [ ] Add one neutral sentence: "A separate, optional research study may ask to use course records; it will be explained by someone who does not teach or grade this course, and taking part or not has no effect on your grade."
5. **People:**
   - [ ] The third party (consent collector and honest broker) is booked for a 5-minute class visit in the last week of classes (April 20 to 23), with the approved script from [../irb/recruitment-script.md](../irb/recruitment-script.md).
   - [ ] TAs told: they may proctor the transfer check but must never see consent status.

## Additional setup for the full-set courses

Random assignment of students is what Northeastern's DHR says "would probably not be exempt", so a full-set section probably puts the application into expedited review. Only build these if the IRB application includes them.

- [ ] Concepts split into sets A and B of similar difficulty.
- [ ] Three spaced retrieval quizzes per set (weeks 4, 7 and 10) and one week-12 retention quiz covering both sets.
- [ ] 6 to 10 hinted practice problems, each with a partial and a full structural hint, built as two quiz versions.
- [ ] After add/drop (ends January 26): randomize the roster into two lists; assign retrieval and hint versions by list; keep the lists private.

## The term, week by week

Spring 2027 dates from Northeastern's 2026–2027 academic calendar (marked "subject to change"). Classes start Wednesday, January 13; spring break is March 8 to 14; the last day of classes is April 25; finals run April 26 to May 2; grades are due Tuesday, May 4 at 2:00 p.m.

| Week | Dates | Every course | Full-set courses only |
|---|---|---|---|
| 1 | Jan 13 to 15 | Calibration mini-lesson (5 minutes); confidence ratings start on every quiz | |
| 2 | Jan 18 to 22 (no class Jan 18, MLK Day) | Core concepts begin (weeks 2 to 6 are the targets of the transfer check) | |
| 3 | Jan 25 to 29 | Add/drop ends Jan 26: freeze the roster for the study | Randomize the two lists |
| 4 | Feb 1 to 5 | Weekly quizzes with confidence ratings and coded distractors continue all term; milestone commits all term | Retrieval quiz 1 (set A to list 1, set B to list 2); hinted practice begins |
| 6 | Feb 15 to 19 (no class Feb 15, Presidents Day) | | |
| 7 | Feb 22 to 26 | | Retrieval quiz 2 |
| | Mar 8 to 14 | Spring break | |
| 10 | Mar 22 to 26 | | Retrieval quiz 3 |
| 11 | Mar 29 to Apr 2 | | Hinted practice ends |
| 12 | Apr 5 to 9 | | In-class retention quiz (both sets) |
| 13 | Apr 12 to 16 | In-class, paper, proctored transfer check (completion credit) | |
| 14 | Apr 19 to 23 (no class Apr 19, Patriots Day) | Third-party recruitment visit, instructor out of the room; forms sealed | |
| After May 4 | | Honest broker opens forms, follows up by email with absent students, exports and de-identifies consenting students' records | |

## Keep a dated record

Log the date each instrument actually ran, and anything that went differently from this plan, in `courses/spring-2027-log.md` (create it in week 1; record dates and events only, never student names or data). Paper 2's methods section is written from that log, and deviations from the pre-registration have to be reported.
