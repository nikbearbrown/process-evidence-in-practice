# Process Evidence in Practice (Frictional, Paper 2)

**A classroom study of agent-run audits for assessment.**

[Read the outline](paper2-outline.md) · [Contributor guide](CONTRIBUTING.md)

## Abstract

*Working abstract. No manuscript exists yet, so this describes what the paper sets out to do. It reports no results.*

Paper 1 tests whether the Frictional auditor detects what it claims to detect on synthetic data. This paper asks whether its findings help instructors assess real student work, and at what cost. It is a classroom study of about 200 students in the author's Spring 2027 courses, under IRB review, with opt-in consent collected by a third party and the instructor blind to consent until grades are posted. In the recommended design, the instructor assesses each submission without the audit report and then with it, and records any change. We plan to report the precision of findings on real work, how often findings change an assessment, the added review time, which dimensions instructors enable, and how often confounds such as squash merges and offline work occur.

## Where the draft is

There is no draft yet. The closest document is the section-by-section outline, [paper2-outline.md](paper2-outline.md).

## What needs to be done

- Submit the IRB application by December 4, 2026.
- Settle the open decisions in the outline that the application depends on.
- Build the instruments into the Spring 2027 courses before January 13, 2027.
- Have a version of the auditor that has passed Paper 1's benchmark.

The full list, in order, is under [The steps, in order](#the-steps-in-order).

## How to contribute

Read the [contributor guide](CONTRIBUTING.md) first. This is a human-subjects study, so who may do what is limited. Anyone with access can review the design, the measures and the wording of the instruments. Only people named on the approved protocol can do anything that touches student work.

## Executive summary

**What this is:** the working repository for Paper 2 of the Frictional program. The working title is *Process Evidence in Practice: A Classroom Study of Agent-Run Audits for Assessment*. It is the classroom study: about 200 students in the author's Spring 2027 courses, under IRB approval. Instructors use reports from the Frictional audit skill, and the study measures whether the findings are accurate on real work, whether they change assessments, and what they cost in review time. The folder will be renamed to match the title you sign off on.

**Why read it:** Paper 2 runs on a fixed clock. Spring 2027 classes start **Wednesday, January 13, 2027**. Before then the study needs:
- an IRB determination. Submit to the Department of Human Research (DHR) by **Friday, December 4, 2026**; its median turnaround for new exempt and expedited applications is 10 business days.
- a reply from the Office of the General Counsel on FERPA;
- instruments built into the courses;
- a version of the audit skill that has passed Paper 1's synthetic benchmark.

**Where it stands (2026-11-22):**
- **The outline and IRB notes are ready for your sign-off:** [paper2-outline.md](paper2-outline.md) and [irb-protocol-notes.md](irb-protocol-notes.md).
- **The IRB, consent and course drafts in [irb/](irb/) and [courses/](courses/) were written for the earlier study design.** That design validated a learning score against a transfer check, and used Fall 2026 records. [irb-protocol-notes.md](irb-protocol-notes.md) §11 lists what changes in each.
- **The skill does not exist yet.** Paper 1 (`../auditing-the-making`) specifies how it is tested. The shared sources and the claims ledger for both papers live there.
- **Nothing has been submitted, sent or changed in any course.** No student work was opened. One disclosure: before the outlining brief, the session counted student folders by file name in four course repositories. Those counts are in [courses/README.md](courses/README.md); remove them if you prefer.

## The steps, in order

### Now to December 4, 2026 (fall break is November 25 to 29)

| # | Step | Done when |
|---|---|---|
| 1 | **Fix the preprint's "labeled corpus" sentence** on nikbearbrown.com. No labeled corpus exists. | The live page no longer says one exists |
| 2 | **Sign off, or change, the Phase 1 deliverables**, especially Paper 2 open decisions 2 (is every submission audited as course practice?), 3 (the review design) and 6 (RQ6). The IRB application depends on them. | Signed or annotated |
| 3 | **Check CITI training:** the "Human Subjects Research, Stage 1 Basic Course" under the Northeastern affiliation, valid 3 years. Responsible Conduct of Research courses do not count. | Certificate valid into 2028 |
| 4 | **Choose the third party**: the honest broker who recruits, holds consent forms and the code key, and de-identifies data. They need the same CITI course. | Agreed |
| 5 | **Confirm the Spring 2027 courses, assignments and teaching assistants.** | Listed in [courses/README.md](courses/README.md) |
| 6 | **Email the DHR** (IRBReview@northeastern.edu) with the questions in [irb-protocol-notes.md](irb-protocol-notes.md) §5 and §8. | Answers in hand |
| 7 | **Email the Office of the General Counsel** about FERPA, with the questions in §7 of the IRB notes. | Reply, or their contact named in the application |
| 8 | **Revise the drafts in [irb/](irb/)** as listed in §11 of the IRB notes. Fill in the DHR application form, add the "AI Systems Used in Human Subjects Research" form, and email everything to IRBReview@northeastern.edu. | Submitted by **December 4** |

### December 2026 to January 12, 2027

| # | Step |
|---|---|
| 9 | Build the Frictional skill and run Paper 1's benchmark v1. The version used in class is frozen only after it passes. |
| 10 | Revise [courses/](courses/) for the audit design: commit discipline, README requirements, the process log, the push record, the two-pass review log, and the course policy that findings are never the sole basis for a grade or integrity action. |
| 11 | Write the marking guide (accurate, inaccurate, can't tell; relevance from 1 to 5; what counts as a changed assessment) and date it. |

### Spring term (January 13 to April 25, 2027; spring break March 8 to 14)

| # | Step |
|---|---|
| 12 | Instruments run from the first day. Audits run on submissions per open decision 2. Instructors and TAs record two-pass reviews, markings and times. |
| 13 | Pre-register the analysis on OSF before May 4, 2027. |
| 14 | Third-party recruitment in the last week of classes (April 20 to 23); forms sealed. |

### After grades (due Tuesday, May 4, 2027, 2:00 p.m.)

| # | Step |
|---|---|
| 15 | Honest broker opens forms, emails absent students, and exports and de-identifies consenting students' records. |
| 16 | Analysis as pre-registered; then writing; venue per the outline. |

## IRB facts this plan rests on (checked 2026-11-22)

- **Applications go by email** to IRBReview@northeastern.edu. The DHR's guidance pages name no online portal.
- **Exempt work cannot start until the investigator has the DHR's determination letter.**
- **Policy 505** (revised May 16, 2025): faculty "may not recruit students from their classes for their own research projects unless prior approval or exemption determinations for the project have been obtained from the DHR."
- **The DHR guidance "Recruiting and Enrolling Your Students"** recommends:
  - a third party to recruit and consent;
  - the instructor not knowing who participates;
  - third-party anonymization;
  - recruitment at the end of the semester.

  It says FERPA "likely applies" to coursework, and that the Office of the General Counsel must be consulted.
- **The DHR's exemption guidance:** a study that "randomly assigns students to different instructional strategies/curricula for comparison, would probably not be exempt."
- **Median turnaround:** 10 business days for new exempt and expedited applications; 3 business days for modifications.
- **Training:** CITI Human Subjects Research Stage 1 Basic Course, valid 3 years.

## Sources

- DHR: [Get Started](https://dhr.research.northeastern.edu/getstarted/); [Review types and processes](https://dhr.research.northeastern.edu/wp-content/uploads/2023/08/Review-types-processes-07.15.2023.pdf); [training](https://dhr.research.northeastern.edu/training); [Fall 2025 newsletter (turnaround times)](https://dhr.research.northeastern.edu/fall-2025-irb-newsletter); [Recruiting and Enrolling Your Students](https://dhr.research.northeastern.edu/wp-content/uploads/2025/05/Recruiting-and-Enrolling-Your-Students.pdf); [Exemption categories and examples](https://dhr.research.northeastern.edu/wp-content/uploads/2023/05/Exemptions-categories-examples-08.22.2023.pdf); [AI Systems form announcement](https://dhr.research.northeastern.edu/new-form-ai-systems-used-in-human-subjects-research-9-8-2025/)
- Northeastern: [Policy 505](https://policies.northeastern.edu/policy505); [2025 change allowing faculty to recruit their own students](https://dhr.research.northeastern.edu/spring-2025-newsletter-special-edition/); [2026–2027 academic calendar](https://registrar.northeastern.edu/wp-content/uploads/sites/9/2026-2027-Academic-Calendar.pdf) (marked "subject to change")
- Federal: [45 CFR 46.104](https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-A/part-46/subpart-A/section-46.104); [34 CFR 99.30](https://www.ecfr.gov/current/title-34/subtitle-A/part-99/subpart-D/section-99.30); [34 CFR 99.31](https://www.ecfr.gov/current/title-34/subtitle-A/part-99/subpart-D/section-99.31)

## Files

| Path | What it is | Status |
|---|---|---|
| [paper2-outline.md](paper2-outline.md) | Paper 2 outline: titles, contribution, research questions, design, section claims and evidence, figures, metrics, threats, related work, venues, open decisions | Phase 1, awaiting sign-off |
| [irb-protocol-notes.md](irb-protocol-notes.md) | Topics the protocol must address, and questions for the DHR. Not legal or regulatory advice. | Phase 1, awaiting sign-off |
| [irb/application-draft.md](irb/application-draft.md), [irb/consent-form-draft.md](irb/consent-form-draft.md), [irb/recruitment-script.md](irb/recruitment-script.md), [irb/data-management-plan.md](irb/data-management-plan.md) | Drafts from the earlier design | To revise (IRB notes §11) |
| [courses/README.md](courses/README.md), [courses/instruments.md](courses/instruments.md) | Spring 2027 setup and dated calendar, from the earlier design | To revise |
| [study/measures.md](study/measures.md) | Definitions of the preprint's starter components and the transfer-check analysis | Applies to the optional secondary analysis |
| [probe-i9-report.md](probe-i9-report.md) | What changed when the comprehension probe was added as instrument I-9, and what is still open | Drafted 2026-11-23, awaiting review |
| `../auditing-the-making/` | Paper 1, `PROJECT.md` (sources), the claims ledger for both papers, verified references | — |

**Never put student data in this repository.** The `.gitignore` blocks `data/`, `exports/` and `consent/`. Keep the repository private.
