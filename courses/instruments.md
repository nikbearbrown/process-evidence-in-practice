# The instruments to build into every Spring 2027 course

> **Status (2026-11-22):** written for the earlier study design, which validated a learning score against a transfer check and used Fall 2026 records. Paper 2 is now a classroom study of the Frictional audit. What changes in this file is listed in [irb-protocol-notes.md](../irb-protocol-notes.md) §11.

## Executive summary

**What this is:** the specification for each measurement instrument that next semester's courses need so the Frictional paper can be tested: what the instrument is, which GLP component it feeds, how to build it in Canvas or GitHub, and what it costs in instructor time.

**Why read it:** every instrument here has to exist *before* the first day of class. Data that was not designed in cannot be recovered later; that is why the past semesters can support only a feasibility paper.

**What it decides:** eight instruments, split into a core set that every course gets (cheap, already partly in place) and a full set for the one or two courses that will carry the validation study. Each instrument is also sound teaching on its own (retrieval practice, spacing, confidence ratings and hints are established good practice), so students who do not consent to the research lose nothing and are asked to do nothing extra. That is what keeps the core set inside "normal educational practice" for the IRB; the two full-set instruments randomize students and probably need expedited review.

## The eight instruments at a glance

| # | Instrument | Feeds | Core or full | Where it lives | Build effort |
|---|---|---|---|---|---|
| I-1 | Milestone commits with pre-rated difficulty | Y₁, Y₂ | Core | GitHub (course repo) | Low: split each assignment into 3 to 4 milestones, rate each 1 to 5 before term |
| I-2 | Frictional log (FRICTIONAL.md), unchanged | Y₅ | Core | GitHub (already in place) | None: already graded at 10% |
| I-3 | Confidence rating after every quiz item | Y₄ | Core | Canvas quizzes | Low: one extra question per item |
| I-4 | Misconception-coded quiz distractors | Y₂ | Core | Canvas quizzes + item bank | Medium: each distractor tagged with a named misconception |
| I-5 | Near and far transfer item pairs | Y₃ | Core | Canvas quizzes + item bank | Medium: two items per core concept |
| I-6 | Counterbalanced spaced retrieval quizzes | Y₆ | Full | Canvas quizzes, two student groups | Medium: concept sets A and B, randomized groups |
| I-7 | Randomized hint levels | Y₇ | Full | Canvas quizzes or notebook problems | Medium to high: partial and full hint for each hinted item |
| I-8 | Delayed, proctored transfer check | Criterion (ground truth) | Core | In class, paper, final two weeks | Medium: 6 to 10 new transfer items on early-term concepts |

Plus the artifact score you already have: the implementation and explanation component of each assignment (60% of the assignment grade) is the artifact quality score **A** that the information gain test compares GLP against.

## I-1. Milestone commits with pre-rated difficulty (Y₁, Y₂)

**What:** each assignment is split into 3 or 4 named milestones (for example: plan, first working version, tests pass, write-up). Students commit at the end of every working session, not just at submission. Before the term starts, you rate each milestone's difficulty from 1 to 5 and record it in the item bank.

**Why:** Y₁ asks whether time tracks difficulty. Without a difficulty number per milestone, set before seeing student data, Y₁ cannot be computed, and a difficulty rating chosen after seeing the data would be circular.

**How:**
- Add a "commit when you stop working" line to `prerequisites/frictional.md` in each course repo. The Frictional rubric already asks for "dated entries connected to commits", so this is a sharpening, not a new rule.
- Ask students to commit with their GitHub no-reply address (Settings → Emails → "Keep my email addresses private"), so a public course repo does not publish their personal email. This is a privacy improvement whether or not the research happens.
- Record difficulty ratings in a private file outside the public course repo (for example in this repo under `study/`, never under `courses/` if the course repo is public).
- After the term, replace the rating with an empirical difficulty as a check: the share of the class that met the milestone on first submission. Report both.

**What it cannot tell you:** commit times show when work was saved, not how hard someone was thinking. Long gaps can be sleep, other courses, or work done elsewhere. Treat Y₁ as a weak signal and say so.

## I-2. The Frictional log, unchanged (Y₅)

**What:** the FRICTIONAL.md process log students already keep, graded on the five-criterion, 10-point rubric in each course's `prerequisites/frictional.md`.

**Why:** it is already the richest Y₅ source you have, and changing it now would break comparability with Fall 2026.

**One change to consider:** none to the student-facing rules. The research coding (φ₁ to φ₄) is separate from grading and is done after the term by coders who are not grading.

**Known confound, to state in the paper:** the log is graded and the rubric is public, so students write *to the rubric*. A graded log is a performed trace, not a covert one. This cuts both ways: it makes Y₅ easier to game, and it makes the log a fair test of whether a gameable trace still carries signal. Say this plainly in the limitations.

## I-3. Confidence rating after every quiz item (Y₄)

**What:** after each quiz question, one more question: "How sure are you of that answer?" with five choices: 0%, 25%, 50%, 75%, 100%. It earns no points and costs none.

**Why:** Y₄ (calibration) cannot be computed from anything collected so far. This is the cheapest new instrument and the one most likely to show something.

**How in Canvas:** add a multiple-choice companion item after each scored item, set to 0 points, or use a single "rate your confidence for questions 1 to 6" item with one dropdown per question. Export results with the Canvas student analysis report; each row is a student and each column an item. Test the export on a dummy quiz before term, because Classic Quizzes and New Quizzes export differently.

**Teach it:** spend five minutes in week 1 showing the class a calibration plot. Calibration is a learnable skill and the course already teaches it (computational skepticism, metacognitive facet). This is what makes it normal educational practice and not a research add-on.

## I-4. Misconception-coded distractors (Y₂)

**What:** every wrong answer choice on a weekly quiz is written to match one named misconception, and each misconception has a code. Before the term, you also write a short map of which misconceptions are one step apart (a student who stops believing M3 typically passes through M5 next). That map is the adjacency matrix **A** for Y₂.

**Why:** Y₂ is computed from the sequence of misconceptions a student shows over time. Without coded distractors, wrong answers are just wrong.

**How:** keep the item bank as a spreadsheet or Markdown table in this repo (private), one row per answer choice: `item_id, choice, correct?, misconception_code, concept, near_or_far, week`. Have a second person (a TA or colleague) check the adjacency map before term, and record where you disagreed.

**Correction to the preprint this forces:** if errors are random, Y₂ is not 0. It equals the share of misconception pairs that are adjacent in **A** (the density of the map). Y₂ has to be reported against a shuffled baseline. See [study/measures.md](../study/measures.md).

## I-5. Near and far transfer item pairs (Y₃)

**What:** for each core concept, two items: a near-transfer item (same kind of problem as taught, new numbers or names) and a far-transfer item (same underlying structure, different surface: a new domain, a new representation, or a new question form).

**How:** tag both items with the same concept code in the item bank. Use Barnett and Ceci's (2002) dimensions (knowledge domain, physical context, temporal context, functional context, social context, modality) to say *what* makes the far item far. Write this down per item; reviewers will ask.

## I-6. Counterbalanced spaced retrieval (Y₆)

**What:** split each course's core concepts into two sets, A and B, of similar difficulty. Randomly assign students to two groups. Group 1 gets spaced retrieval quizzes (three short low-stakes quizzes at increasing gaps, weeks 4, 7 and 10 in Spring 2027) on set A; Group 2 gets them on set B. Everyone gets the same number of retrieval questions; only the concepts differ. A short in-class retention quiz in week 12 covers both sets and gives Y₆. The transfer check (I-8) also covers both sets but is kept separate, so Y₆ never leaks into the criterion.

**Why this design:** the preprint's Y₆ needs a treatment and a control condition. Giving some students spacing and others none would withhold a known benefit. Counterbalancing within students gives every student spacing on half the material, lets each student serve as their own control, and keeps the design within normal educational practice.

**How:** randomize the roster into two lists after add/drop ends (January 26, 2027) and keep the lists private. Canvas's "Assign to" setting on a quiz accepts individual students, so give each retrieval quiz to one list. Check on a test course before term that the gradebook shows "not assigned" (not zero) for students outside the list.

**Full set only, and an IRB question:** do this in the one or two courses carrying the validation study, not everywhere. Northeastern's DHR says a study that randomly assigns students to different instructional strategies "would probably not be exempt", so including this instrument probably means expedited review. Include it only if the application does.

## I-7. Randomized hint levels (Y₇)

**What:** for a small set of practice problems (6 to 10 per term), a student who gets the problem wrong on the first try is shown either a *partial structural hint* or a *full structural hint*, chosen at random per student and per problem, and then tries again.

**Why randomize:** the preprint's ladder (no hint, then partial, then full) confounds the full hint with having already seen the partial one. Randomizing which hint a student sees gives clean estimates of each hint's effect.

**How:** two versions of each hinted practice quiz, one with partial hints and one with full hints, assigned to the same two student lists as I-6 but crossed with problem (list 1 gets partial hints on odd problems and full hints on even ones, list 2 the reverse). In Canvas the simplest build is a practice quiz with two allowed attempts: the hint goes in the question's wrong-answer feedback, shown after attempt 1, and attempt 2 is the retry. Confirm the feedback setting on a test course first. In notebook courses, the same logic in the notebook.

**Full set only, with the same IRB caveat as I-6.** The per-student Y₇ estimate from 6 to 10 items is noisy; Paper 2 should report it at the group level first.

## I-8. Delayed, proctored transfer check (the independent criterion)

**What:** a 20 to 30 minute in-class, paper, no-device check in the last two weeks of term. It has 6 to 10 *new* near and far transfer items on concepts taught in weeks 2 to 6, drawn from both retrieval sets A and B. Students know there will be an in-class check; they do not see the items or the concepts in advance.

**Why:** this is the ground truth GLP is tested against. It is independent of every in-course trace (different time, different setting, no AI available, items never seen), which is what fixes the circular validation in Section 7 of the preprint.

**Grading:** completion credit only (for example, a participation point), so a surprise item can never cost a student their grade. Fold it into the existing paper-exam logistics if that is simpler, but keep these items out of the graded score.

**Proctoring:** TAs can proctor; they do not see consent status.

## The contrast condition is not a course instrument

Agents completing the same assignments give the "known borrowed" anchor. That needs no students and no IRB; now part of Paper 1's synthetic benchmark (`../auditing-the-making/synthetic-benchmark-spec.md`).
