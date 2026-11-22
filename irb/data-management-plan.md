# Data management and de-identification plan (draft for the IRB)

## Executive summary

**What this is:** how student records move from the course to the analysis without identifying anyone: who holds what, how identifiers are removed, where data are stored, and what may appear in a paper.

**Why read it:** removing names is not enough here. The course repositories are public on GitHub, student folders are named by first name and last initial, commit histories carry usernames and emails, and a distinctive log sentence can be found with a web search. The IRB will ask how each of those is handled; this is the answer.

**What it decides:** an "honest broker" (the same third party who collects consent) exports and de-identifies the records of consenting students only, after grades are submitted. The researcher works only with the coded data set. Papers report numbers and charts of derived features; quotes appear only with consent and only after a search check.

## Who holds what

| Person | Holds | Never holds |
|---|---|---|
| Third party / honest broker | Consent forms, the code key, raw exports of consenting students' records | Grades authority; any role in the course |
| Researcher (instructor) | The de-identified analysis data set | The consent list (or, if the IRB allows, receives it only after final grades) |
| Coders (Y₅) | De-identified log entries | Names, folders, repository links |
| Collaborators outside Northeastern (for example Humanitarians AI fellows) | De-identified data only, and only if named in the approved protocol | Anything identifiable |

## Steps, in order

1. **Term ends; grades submitted.** Nothing is exported before this.
2. **Export (honest broker).** For consenting students only: FRICTIONAL.md files, git history (`git log` with times, messages, diffs), Canvas quiz reports, gradebook columns used in the study. Records of students who did not consent are never exported.
3. **Replace identifiers.** Each student gets a random code. Removed or replaced: names and initials, folder names, GitHub usernames, commit author names and emails, Canvas IDs, repository URLs, and any name, employer, hometown or other personal detail inside log text.
4. **Blur time without losing intervals.** Absolute dates are shifted by a random per-course offset; intervals between commits and the day-of-term are kept, because Y₁ needs them.
5. **Hand over.** The coded data set goes to the researcher; the key stays with the honest broker.
6. **Destroy the key** on [date], after which withdrawal is no longer possible (the consent form says so).

## What may appear in a paper

- **Derived features only, by default:** correlations, commit cadence charts, calibration plots, coded marker scores. No raw logs, no code.
- **Quotes** only from students who ticked the quoting box, lightly paraphrased if needed, and only after the exact quote is searched on GitHub and a general web search and returns nothing.
- **Case studies** only from students who ticked the case-study box, as composites or abstracted descriptions, and reviewed by the student before publication.
- **Small cells:** no statistic is reported for a group of fewer than 5 students; a course section with fewer than 10 consenting students is reported only pooled with others.

## Storage

- Raw exports and the key: a Northeastern-approved storage location for restricted student data, owned by the honest broker. Ask the IRB or Northeastern ITS which service is approved for FERPA-protected research data.
- The de-identified data set: the same approved storage. Not in a public repository, and not in this repository unless this repository stays private and the IRB approves it.
- **AI tools:** if any step (for example coding Y₅) uses an AI model on student text, the application names the tool, and only a Northeastern-licensed service with a data agreement is used. Never paste student records into a personal account.
- **Retention:** de-identified data kept for [the period Northeastern's HRPP requires after study closure], then deleted.

## The agent contrast runs

Agent-generated repositories, logs and transcripts contain no student data and may be stored and shared freely.
