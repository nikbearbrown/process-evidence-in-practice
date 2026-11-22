# The agent contrast condition

## Executive summary

**What this is:** the plan for having AI coding agents complete the same course assignments students do, while capturing the same process traces (commits, timing, quiz answers with confidence, a FRICTIONAL.md log). Their traces are the "known borrowed" anchor the paper compares students against.

**Why read it:** it replaces the preprint's use of academic integrity cases as labels, which is ethically fraught (misconduct records become training data) and biased (only students who were caught). Agents involve no students, so this work **needs no IRB and can start now**, while the IRB application is under review.

**What it does not do:** agent traces mark the extreme end of the spectrum. Real students who use AI are hybrids, so the paper must not treat "looks like the agent" as "is borrowed". It also tests Claim 03 (gaming costs as much as learning) directly: an agent told to fake human-looking traces is the red-team study, without recruiting anyone.

## Three agent conditions per assignment

| Condition | Instruction to the agent | What it represents |
|---|---|---|
| **Plain** | Complete the assignment. | Fully borrowed work with no attempt to hide it |
| **Logged** | Complete it, commit after each step, and keep FRICTIONAL.md as the course asks. | Borrowed work that follows the process rules |
| **Gaming** | Complete it so that the commit history, timing and log look like a student who struggled and learned: paced commits, plausible errors fixed in a sensible order, a specific and uncertain log. | The red-team: manufactured friction traces |

Run each condition at least 5 times per assignment, so there is a distribution, not one example. Use the agent tools students actually have (Claude Code and Codex at minimum). Bulk runs go through headless `claude -p` on the Claude plan, not an API key.

## What to capture

- The full git history (commit times, messages, diffs) in a fresh repository per run.
- The FRICTIONAL.md log, for the Logged and Gaming conditions.
- Answers to the course quizzes with a confidence rating per item, given by the agent under the same instructions.
- The agent session transcript, kept with the run.

Store runs under `study/agent-runs/<course>/<assignment>/<condition>-<n>/` in this repo (private). The runs contain no student data.

## What Paper 1 reports

- Y₁, Y₂* and Y₅ distributions for each agent condition, beside the consented student cases.
- Which traces the Gaming condition manages to fake, and at what cost (agent time, tokens, how many tries). This is the first evidence for or against Claim 03.
- Where agent traces and student traces overlap. Overlap is a finding, not a failure.

## A fourth, optional condition: instructor with an agent

The instructor's own example folders (the course repos' `nik-bear-brown/` folders, where assignments are done with Claude and logged in FRICTIONAL.md) are a hybrid condition: a person who already knows the material, working with an agent. Because it is the author's own data it involves no students. Ask the IRB in the same application whether they want it listed; most treat self-study as not human subjects research, but let them decide.
