# How each measure is computed

> **Status (2026-11-22):** written for the earlier study design, which validated a learning score against a transfer check and used Fall 2026 records. Paper 2 is now a classroom study of the Frictional audit. What changes in this file is listed in [irb-protocol-notes.md](../irb-protocol-notes.md) §11.
>
> **Update (2026-11-23):** the section "Probe receipts (instrument I-9)" added by Claude Code (Claude Opus 5.5) for the owner's review.

## Executive summary

**What this is:** operational definitions for every quantity the two papers will report: the seven GLP components, the artifact score, the independent criterion, and the information gain test. It fills the gaps the review found in the preprint's Section 4 and Section 7.

**Why read it:** these definitions have to be fixed, and pre-registered, *before* anyone looks at Spring 2027 data. A definition chosen after seeing the data would let the result pick the measure.

**What it decides:** Paper 1 computes only Y₁, Y₂ and Y₅ and claims only that they can be computed. Paper 2 computes all seven against the delayed transfer check. Four corrections to the preprint come out of writing the definitions down: Y₂'s chance level is not zero, Y₃ is defined two different ways, Y₄_dir has no definition, and "credible interval" is the wrong name for what the ensemble produces.

## Notation

- Student *s*, concept *c*, assignment milestone *m*, quiz item *i*.
- **A**: artifact quality score, the implementation and explanation component of each assignment (already graded, 60% of each assignment), averaged over the term.
- **T**: score on the delayed, proctored transfer check (instrument I-8). This is the criterion. It is never used to build any GLP component.

## Y₁ Temporal Engagement Pattern

- **Difficulty d_m:** the instructor's 1 to 5 rating of milestone *m*, recorded before term. Sensitivity check: empirical difficulty, 1 minus the share of the class who met milestone *m* on first submission.
- **Time τ_s,m:** estimated active time on milestone *m*, from commit timestamps. Consecutive commits less than *g* minutes apart count as one working session; the session's span is its time. Pre-register *g* = 45 minutes, with 30 and 60 as sensitivity checks. Commits to a milestone's files are assigned to that milestone.
- **Y₁(s) = Spearman correlation of d and τ across student *s*'s milestones.** Spearman, not Pearson, because both are ordinal-ish and skewed.
- **Minimum data:** at least 8 milestones per student, or Y₁ is reported as missing.
- **Limitation to state:** commit time measures when work was saved, not effort.

## Y₂ Error Trajectory Coherence

- **Errors e_s,1, e_s,2, …:** the misconception codes of the wrong answers student *s* chose, in time order (instrument I-4). In code courses with an autograder, failing-test categories per commit can be used instead; say which in each course.
- **Adjacency A(m, m′):** 1 if misconception *m′* is a named next step from *m* in the map written before term, else 0. Two people build or check the map; report their agreement.
- **Raw Y₂(s) = Σ A(eᵢ, eᵢ₊₁) / Σ 1[eᵢ ≠ eᵢ₊₁]** as in the preprint.
- **Correction:** under random errors, raw Y₂ is not 0. Its expected value is the density of **A** among the misconceptions the student could have reached. So report **Y₂*(s) = raw Y₂(s) − mean raw Y₂ over 1,000 within-student shuffles of the same errors.** Y₂* ≈ 0 is the "no coherent model" signature; Y₂* > 0 is coherence.
- **Minimum data:** at least 6 transitions between distinct misconceptions.

## Y₃ Cross-Context Transfer

- **ρ_near(s), ρ_far(s):** proportion correct on near-transfer and far-transfer items (instrument I-5), in-course quizzes only. The items on the transfer check (I-8) are never used here.
- **Correction:** the preprint defines Y₃ as a weighted sum (0.4 ρ_near + 0.6 ρ_far) but describes the borrowed signature as a large near-far *gap*. These are different quantities. Use the gap, **Y₃(s) = ρ_near(s) − ρ_far(s)**, where *smaller* is the genuine signature, and report overall accuracy separately. The weighted sum mixes ability with transfer.

## Y₄ Uncertainty Calibration

- **Confidence cᵢ** in {0, 0.25, 0.5, 0.75, 1} from instrument I-3; **correctness rᵢ** in {0, 1}.
- **Brier score B(s) = mean (cᵢ − rᵢ)².**
- **Reference B_ref(s) = ρ(s)(1 − ρ(s))**, the Brier score of always answering with one's own overall accuracy ρ(s). This is the standard Brier skill score reference.
- **Y₄(s) = 1 − B(s) / B_ref(s).** Positive is better calibrated than the reference.
- **Y₄_dir(s) = mean (cᵢ − rᵢ)**, the overconfidence bias. This is the definition the preprint names but never gives. Positive is overconfident.
- **Minimum data:** at least 30 rated items.

## Y₅ Social Knowledge Texture

- **Source:** FRICTIONAL.md entries (instrument I-2); discussion posts if the course has them.
- **Coding:** each entry is scored on four markers, each **0, 1 or 2** (absent, present but generic, specific and anchored):
  - φ₁ personal encounter: a confusion, surprise or decision that is specific to this student's attempt.
  - φ₂ below-surface engagement: names a mechanism or reason, not only a result.
  - φ₃ productive uncertainty: states what is still not understood, specifically.
  - φ₄ real-time development: a position or plan that changed, and why.
- **Y₅(s) = (φ₁ + φ₂ + φ₃ + φ₄) / 8**, averaged over the student's entries, in [0, 1].
- **Raters:** two coders who did not grade the course, trained on 20 entries from consenting students outside the analysis set, then double-coding 20% of the analysis set. Report Cohen's weighted kappa per marker; target ≥ 0.6. If any coding uses an AI model, the IRB application must say which tool, and the data must stay inside a Northeastern-approved service.
- **Confound to state:** the log is graded on a public rubric (see the courses doc, I-2).

## Y₆ Retrieval Strength Decay Signature

- From the counterbalanced design (instrument I-6): student *s* had spaced retrieval on concept set A or B.
- **Retention items:** a short in-class retention quiz in week 12 with items on both concept sets, separate from the transfer check.
- **Y₆(s) = proportion correct on the week-12 retention items for the student's spaced set − proportion correct for the unspaced set.** Positive is the spacing benefit.
- **Do not compute Y₆ from the transfer check (I-8).** That would make Y₆ part of the criterion it is being tested against. Pre-register this.

## Y₇ Scaffolding Response Curve

- From randomized hint levels (instrument I-7): for each hinted problem, the student saw either a partial hint (h₁) or a full hint (h₂) after a wrong first attempt.
- **Gains:** g₁(s) = retry success rate after partial hints; g₂(s) = retry success rate after full hints; h₀ baseline is first-attempt success.
- The preprint's ratio [ρ(h₁) − ρ(h₀)] / [ρ(h₂) − ρ(h₀)] is unstable when the denominator is near 0. **Use the bounded form Y₇(s) = g₁(s) / (g₁(s) + g₂(s))**, or report g₁ and g₂ separately. Report at group level first; per-student estimates from 6 to 10 items are noisy.

## Probe receipts (instrument I-9)

`frictional probe receipts` turns a student's receipts into separate evidence packets. Nothing adds them into a GLP score. Each number describes answers given under recorded conditions (no AI, no notes); none measures learning, authorship or AI use.

| Component | Probe rows | Minimum-data limit |
|---|---|---|
| Y₁ | each item's start and end time, with the difficulty fixed at freeze (low, medium, high) | Y₁ above is Spearman over at least 8 rated units; a probe has 6 to 8 items, and the timeboxes and hint ladder cut off the longest. Do not merge with milestone times: different grain, different difficulty scale. Intervals extended for an accommodation are left out. |
| Y₃ | near and far items, correct or not | one of each per probe, so one probe gives no per-student gap. Pool probes or report for the group. Items differ per student, so keep them apart from I-5 unless pooling is pre-registered. |
| Y₄ | every attempted item with a confidence; on the bug item, correct means fixed with no hint | Y₄ above needs 30 rated items; a probe gives 6 to 8. Probe confidence comes before the item and I-3's after, so any pooling is pre-registered, with the source as a covariate. |
| Y₆ | predict items: share correct by delay from the deadline, forms A and B | a description only, and only if both sessions used the same view. No individual Y₆ (below). |
| Y₇ | the bug item: success at each rung among those who reached it | one bug item per probe. The ladder is conditional, so no ratio and no g₁ or g₂; never pooled with I-7. |
| Y₅ | none: the optional walkthrough rubric is a teaching aid | not a Y₅ source |

The Y₁ and Y₇ packets need two small adapter changes in Frictional that are written but not yet applied (design note, section 11).

**Why there is no individual Y₆ from probes.** Frictional's design note (`docs/probes-design.md`, section 7):

> The preprint defines Y6 = ρ_treatment(t₃) − ρ_control(t₃): the difference, at a long delay, between material that had spaced retrieval and material that did not. A re-probe gives one student's success on the same functions at two delays. That describes change over time. But it mixes forgetting with the testing effect (the first probe is itself retrieval practice), with differences between forms A and B, and with later coursework that reuses the same ideas. With no unspaced material to compare against, it cannot show a spacing effect.

An individual version would need the I-6 contrast inside each student (matched item sets, only one spaced, counterbalanced), parallel forms keyed at each delay, the same view and conditions at every delay, and enough items. The note: "At 60% correct, the standard error of the difference between two sets of n items each is about √(2 × 0.24 / n): 0.35 at n = 4, 0.25 at n = 8, and 0.10 at n = 48. A student's own project has 3 to 5 eligible functions." Its conclusion: "So v1 reports success by delay as a description. Any Y6 is a group-level analysis under the approved protocol." Y₆ in Paper 2 stays the I-6 definition above.

**Pre-register** whether probe rows enter any component, and how (a separate source, pooled with a source flag, or group level only).

## Combining the components

- **Paper 1:** no combined score. Report each computable component separately with its distribution for consented students and for the agent contrast runs.
- **Paper 2:** a pre-registered, transparent combination: standardize each component within course, then either (a) equal weights, or (b) a logistic or linear regression fitted on one course and tested on another. No three-layer ensemble until there is data to fit it.
- **Intervals:** call them what they are. Bootstrap confidence intervals for group statistics; conformal prediction intervals (Angelopoulos and Bates) for an individual student's predicted criterion score. Drop "credible interval" unless Layer 3 is made genuinely Bayesian.

## The information gain test (Paper 2)

The preprint's ΔI needs a labeled "genuine" class. The fix replaces the label with the independent criterion **T**.

- **Model 0:** T ~ A + course (fixed or random effect).
- **Model 1:** T ~ A + G + course, where G is the pre-registered GLP combination.
- **ΔI is reported as ΔR²** (or, if T is dichotomized at a pre-registered cut, Δ AUC and the mutual information difference) with bootstrap confidence intervals.
- **Hypothesis H2 is supported** if the lower confidence bound of ΔR² is above 0. Report per-component increments too.
- **Pre-register on OSF** before the Spring 2027 data are opened: hypotheses, these definitions, the session gap *g*, minimum-data rules, exclusions, and the analysis models.
