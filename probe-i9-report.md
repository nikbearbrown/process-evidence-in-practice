> **Provenance.** Drafted by Claude Code, model Claude Opus 5.5 (`claude-opus-5-5`), on 2026-11-23, from its hand-over note and reports to the owner. Moved into this repository on 2026-11-24, so it survives the deletion of the session notes folder. Nothing was sent to the DHR or anyone else.
>
> **Human sign-off** (left blank until a human fills it in)
> Name: ____________ Date: ____________ Decision (approved / approved with changes / rejected): ____________ Notes: ____________

# Comprehension probe (I-9) in the Paper 2 drafts: what changed

## Executive summary

**What this is:** the list of edits that add Frictional's comprehension probe to this study as instrument I-9. The owner approved adding it to the December 4, 2026 application on 2026-11-23 (Frictional probe design, decision 9a), and approved the follow-up edits to the application draft and the course calendar the same day.

**Why read it:** to review the I-9 wording before the application goes to IRBReview@northeastern.edu by December 4. The edits are in place in the files below; this file only lists them and the points still open.

**What it found:**
- I-9 is drafted in seven files: the instruments, the measures, the IRB notes, the application, the consent form, the data plan and the course calendar.
- **One re-probe, not two.** Frictional accepts one initial receipt and at most one re-probe receipt per student, and form B is predict items only. Two re-probes would need a form C and a code change.
- **Confidence is asked at different times.** Students rate confidence before each probe item; I-3 asks after each quiz item. The drafts keep them as separate Y₄ sources unless pooling is pre-registered.
- **"Core" means not randomized,** not "every course". Version 1 reads Python only, and the instructor's work per project (difficulty ratings, two transfer tasks with reference solutions) grows with class size.
- **No individual Y₆.** A re-probe describes success by delay; it cannot show a spacing effect ([study/measures.md](study/measures.md) quotes the design note).
- **Still open:** real project deadlines, then real probe dates; question 5 for the DHR (does a hint ladder that is not randomized, on the student's own code, stay within normal educational practice, and would randomizing the hints change the category?).

Nothing from a probe may be used for research before the DHR approves the protocol and the student consents.

## Changes by file

| File | What changed |
|---|---|
| [courses/instruments.md](courses/instruments.md) | Status line; "eight" became "nine" instruments; an I-9 row in the at-a-glance table; a new I-9 section: what it is, why, how, core or full, build effort, overlap with I-3, I-5 and I-7, never on the I-8 transfer check, what it cannot tell you, research use |
| [study/measures.md](study/measures.md) | Status line; a new section "Probe receipts (instrument I-9)": how receipts map to Y₁, Y₃, Y₄, Y₆ and Y₇ with each component's minimum-data limit, why there is no individual Y₆ (quoting the design note's section 7), and a pre-registration line |
| [irb-protocol-notes.md](irb-protocol-notes.md) | Provenance line; a summary bullet; §4 procedures; §5 question 5 for the DHR; §6 a probe-files bullet; §9 the install-test row extended to the probe's key run, and two new risk rows; §11 an I-9 row |
| [irb/application-draft.md](irb/application-draft.md) | Status line; a summary sentence; §4 a probe paragraph (what students do and how long it takes); §5 a sentence for each of Part B and Part B', with a bracketed DHR question; §8 the grades row extended and three probe rows; §10 the AI-systems paragraph |
| [irb/consent-form-draft.md](irb/consent-form-draft.md) | Version A: a bracketed sentence (the probe was course practice for everyone, completion credit only, never an integrity check) and a records bullet (receipts, not answers or the sheets that contain the student's code) |
| [irb/data-management-plan.md](irb/data-management-plan.md) | Step 2 exports receipts and the packets derived from them, for consenting students, after grades; specs, sheets, keys and bug variants are never exported. Step 3 replaces the instructor's receipt pseudonyms. |
| [courses/README.md](courses/README.md) | Status line; a summary sentence; the probe in the syllabus item; calendar placeholders (below) |

## What students do (as drafted)

- **Probe, form A, in class, no AI or notes.** Part 1: 3 to 5 predict-the-output items, about 3 minutes each, showing only signatures and docstrings; collected before part 2. Part 2: one injected-bug item (up to 15 minutes, partial hint at 5, full hint at 10) and one near and one far transfer task (about 10 minutes each). At most about 50 minutes.
- **Re-probe, form B, optional.** The same functions with new inputs, predict items only, about 10 to 15 minutes, 4 to 6 weeks after the probe.
- Completion credit only; the same kinds and number of items for every student in a section, on an announced date; never triggered by an audit finding.
- Answer keys come only from a container run of the student's code, never from a model. An AI agent may draft only the transfer-task wording, labelled with its model name, and the instructor approves it before the probe is frozen.

## Calendar placeholders (Python-project courses)

| Week | Dates | Probe step |
|---|---|---|
| 4 | Feb 1 to 5 | First project deadline, end of week |
| 5 | Feb 8 to 12 | Build each probe, rate difficulty, write the transfer tasks, freeze |
| 6 | Feb 15 to 19 | Probe, form A |
| 10 | Mar 22 to 26 | Re-probe, form B, about 5 weeks later (any date in weeks 9 to 11 keeps it 4 to 6 weeks after) |

The window stays clear of the week-12 retention quiz and the week-13 transfer check.

## Sources

- Frictional's design note, `docs/probes-design.md` in [nikbearbrown/frictional](https://github.com/nikbearbrown/frictional), sections 6 to 8 and 10.
- Frictional's `probes.py`: one initial and at most one re-probe receipt per student; the default timings (3 minutes per predict item, 10 per transfer task, hints at 5 and 10, stop at 15).
