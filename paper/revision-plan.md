# Revision plan: from preprint to Paper 1 and Paper 2

## Executive summary

**What this is:** a section-by-section list of what has to change in [frictional.md](frictional.md) to turn it into a submittable paper, and how the material splits between two papers.

**Why read it:** the preprint argues well but claims results it does not have. Reviewers at learning-analytics and computing-education venues will reject it on four points: no data, a validation design that validates itself, unsourced neuroscience numbers, and a thin reference list. Each is fixable, and this file says how.

**What it decides:**
- **Paper 1** is a framework plus experience report: the trimmed framework, the claims restated as hypotheses, Fall 2026 case studies (consented) for the three components that past data can support (Y₁, Y₂, Y₅), and agent-completed assignments as the contrast. It claims feasibility only.
- **Paper 2** is the validation: all seven components from Spring 2027 against the delayed, proctored transfer check, plus the red-team test of Claim 03.
- One factual problem must be fixed before anything else, even on the website: the preprint's closing says "the GLP framework implementation, labeled corpus, and assessment design templates are published openly at irreduciblyhuman.com." No labeled corpus exists yet. Change that sentence to future tense or remove it.

## The four claims, recast as hypotheses

| Preprint claim | Status | Restated as | Test | Paper |
|---|---|---|---|---|
| 01: genuine learning at each tier leaves friction traces arising from neurological processes | Not testable as written | **H1.** In the same assignments, the computable process measures (Y₁, Y₂*, Y₅) of students differ from those of AI agents completing the work. | Compare distributions, consented students vs agent runs (see [study/agent-contrast.md](../study/agent-contrast.md)) | 1 (descriptive), 2 |
| 02: traces are partly independent of artifact quality and add information | Empirical | **H2.** A pre-registered GLP score computed from in-course process data predicts the delayed, proctored transfer check beyond what artifact quality predicts (ΔR² > 0). | Incremental validity, [study/measures.md](../study/measures.md) | 2 |
| 03: gaming all seven costs about as much as learning | Empirical, least supported, most important | **H3.** Agents instructed to fake human-looking traces can raise the traces collected *outside* controlled settings (commits, timing, logs) into the student range, but not those collected in controlled settings (proctored transfer, in-class retention, calibration under proctoring). | The Gaming agent condition; later a human red-team study (IRB amendment) | 1 (agents), 2 |
| 04: a second evidence stream, weighted by the instructor | Design stance | Keep as written. | None needed | 1 |

H3 changes the paper's argument in a useful way: the robustness comes mostly from **where** a trace is collected, not from combining seven of them. Say that, and let the data decide how much the ensemble adds.

## Section by section

### Title and abstract
- Keep "Frictional" as the series name. Paper 1 working title: *Frictional: Measuring the Process of Coursework When AI Can Produce the Product (An Experience Report)*. Paper 2 working title: *Do Process Traces Predict Durable Transfer Beyond Artifact Quality?*
- Rewrite the abstract last, around the hypotheses and what was actually measured. Drop "biological event."

### 1. Introduction
- Keep the framing ("the artifact used to be proof of the process").
- Cite evidence for the detector claims instead of asserting them: studies of AI-text detector accuracy and bias (see [references-to-add.md](references-to-add.md)).
- Soften "permanent" and "predictable winner" to what the evidence supports.
- Replace the sentence that grounds traces in "a cascade of neurological processes" with the behavioral account from the new Section 3.

### 2. The decoupling problem
- Keep 2.1 and 2.3.
- 2.2 "Perverse incentives": cite or soften ("students can learn to game a detector" rather than "students learn to").

### 3. Foundations (rename from "Neurobiological Foundation")
- **Delete** the BDNF "2.8-fold" figure and the dendritic spine "37%" figure. Both trace to one 2026 MDPI review (Gkintoni et al.), whose six cited studies are human imaging and brain-stimulation work that measured neither BDNF nor spines. Neither number has a primary source. Unsourced molecular numbers are the fastest way to lose a learning-sciences reviewer. Details: [references-to-add.md](references-to-add.md#the-neuroscience-figures-remove-do-not-cite).
- Rebuild the section on behavioral cognitive science: desirable difficulties, the testing effect, the spacing effect, storage strength versus retrieval strength, and fluency illusions. Each has a large, replicated literature (see [references-to-add.md](references-to-add.md)).
- Dopamine prediction-error signaling may stay as one sentence of background, cited, not as the link that licenses the measures.
- Replace "It cannot produce the behavioral traces those events leave, because the events did not occur" with the defensible claim: traces can be simulated, but simulating them has a cost, and simulating the ones collected in controlled contexts is hard.

### 4. The GLP framework
- Frame GLP explicitly as an **evidence-centered design** argument (student model, evidence model, task model). This is the standard frame reviewers will expect.
- Position against stealth assessment, gaming-the-system detection, knowledge tracing and keystroke logging (related work section, new).
- Position against commercial process-capture tools (Grammarly Authorship, Turnitin Clarity): they document *who produced the text*; GLP estimates *whether learning occurred*.
- Apply the definitional fixes in [study/measures.md](../study/measures.md):
  - Y₁: difficulty rated before term; time from commit sessions with a pre-registered gap; Spearman.
  - Y₂: chance level is the adjacency density, not 0; report against a shuffled baseline (Y₂*); say how **A** is built.
  - Y₃: the preprint defines a weighted sum but describes a gap; use the gap.
  - Y₄: give B_ref (Brier skill score reference) and define Y₄_dir = mean(c − r).
  - Y₅: state that each φ runs 0 to 2; give the codebook and inter-rater agreement.
  - Y₆: counterbalanced within-student design; never computed from the criterion.
  - Y₇: randomized hint levels; bounded form.
- "E genuine / E borrowed" as a binary is a strong assumption; most real students are hybrids. Say GLP estimates a position on a continuum, operationalized by the criterion.

### 5. Ensemble architecture
- Paper 1: cut to one paragraph. Report components separately.
- Paper 2: a pre-registered transparent combination (equal weights or regression fitted on one course and tested on another).
- Move the three-layer ensemble to "future work"; it needs labeled data at a scale that does not exist.
- "Credible interval" → "confidence interval" (bootstrap) or "prediction interval" (conformal), unless Layer 3 becomes genuinely Bayesian.
- Keep 5.3 "The instructor as meta-model"; it is the paper's best idea about use.

### 6. Tier calibration → Facet calibration
- Replace "tier" with "facet" throughout and drop the numbering, to match the Irreducibly Human framework as now described:

| Preprint | Becomes |
|---|---|
| Tier 1 Pattern | Pattern & Association |
| Tier 2 Embodied | Embodied & Sensorimotor |
| Tier 3 Social | Social & Personal |
| Tier 4 Metacognitive | Metacognitive & Supervisory |
| Tier 5 Causal | Causal & Counterfactual |
| Tier 6 Collective | Collective & Distributed |
| Tier 7 Wisdom | Existential & Wisdom |

- "Tier-sensitive", "tier-calibrated", "tier-conditioned" → "facet-sensitive", "facet-calibrated", "facet-conditioned". Layer 2's "seven combination models, one per cognitive tier" → "one per facet".
- Mark the facet table as hypotheses for future work (H4: the most informative component differs by facet). Neither paper has enough activities per facet to test it.

### 7. Validation
- **Delete** the integrity-case corpus (7.1). It turns misconduct records into labels and only includes students who were caught.
- **Delete** the "confirmed genuine" class built from convergent evidence across the same components (it validates itself).
- **Replace** with the independent criterion (the delayed, proctored transfer check) and the incremental validity test in [study/measures.md](../study/measures.md). Keep 7.2's point about calibration, applied to predicted criterion scores.
- Add pre-registration (OSF) before Spring 2027 data are opened.

### 8. The arms race problem
- Rewrite around H3 and the agent Gaming condition. Report what agents could and could not fake, and at what cost.
- Keep the closing idea ("if gaming every trace requires learning, that is learning") as the hypothesis it is, not a conclusion.

### 9. Discussion
- 9.3 Ethics: expand. Cite learning analytics ethics (Slade and Prinsloo). Describe the consent design (third party, opt-in, instructor blind to consent). Name the two confounds specific to these courses: the Frictional log is graded on a public rubric, and course work is posted in public repositories.
- Add a limitations section: single instructor, graduate courses at one university, self-selected consenting students, commit time is a weak proxy for effort, agents are not students.

### 10. Conclusion, acknowledgments, references
- Fix the "labeled corpus … published openly" sentence (see the summary above).
- Add the IRB protocol number and determination ("This study was reviewed by Northeastern University's IRB, protocol [number], and determined [exempt under …]").
- Add a competing-interests statement covering Humanitarians AI and Bear Brown and Company, and say who funded what.
- Affiliation: Northeastern first, since the data come from Northeastern courses.
- The self-citation to the Musinique paper must point to something a reviewer can find (a preprint URL), or be dropped.
- Reference list: grows from 6 to roughly 30 to 40. See [references-to-add.md](references-to-add.md).

## Paper 1 outline (experience report, about 6 pages plus references)

1. Introduction: the decoupling problem, briefly; the question (can process traces be measured in ordinary courses, and what do they show?).
2. Framework: GLP trimmed to an evidence-centered design argument; the seven components in one table; H1 to H3.
3. Related work: ECD, stealth assessment, gaming detection, knowledge tracing, keystroke logging, calibration, transfer, commercial process capture, ethics.
4. Context: the Fall 2026 courses, the AI policy, the Frictional log and rubric, the GitHub workflow, consent and IRB determination.
5. Method: Y₁, Y₂*, Y₅ as defined; the agent conditions.
6. Results: 3 to 5 consented case studies as derived features; agent distributions; what the Gaming agents managed to fake and at what cost.
7. Lessons for instructors: what was cheap, what was not, what Spring 2027 changed as a result.
8. Limitations and what Paper 2 will test.
