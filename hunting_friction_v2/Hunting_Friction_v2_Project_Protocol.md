# Hunting Friction v2 — Project Protocol

**Repository:** SymC-Universe/Adaptive-Intelligence-Framework  
**Branch:** hunting-friction-v2-rebuild  
**Program governance:** SymC General Operations Manual v0.8.0 (14 September 2026)  
**Current maturity:** P0-D — discovery, reconstruction, Function Map / Limit Map development  
**Legacy paper:** *Hunting Friction: A Multi-AI Adversarial Methodology for Rigorous Independent Research*  
**Legacy DOI:** 10.5281/zenodo.17904511  
**Status of legacy claims:** inherited for audit, not presumed valid

---

## 1. Native scientific question

Does a structured adversarial cross-model research-review protocol provide measurable incremental value over simpler AI-review workflows for detecting, localizing, correcting, and appropriately refusing unsupported research claims under controlled known-truth and research-like tasks?

The project does **not** begin by assuming that adversarial friction is beneficial, that more disagreement is better, that heterogeneous models are independent, that human arbitration is necessarily superior, or that a SymC chi coordinate applies.

The first task is to characterize what actually happens.

---

## 2. Frozen P0-D subquestions

1. Does disagreement or challenge intensity predict latent error detection after ground truth is opened?
2. Does model heterogeneity reduce correlated blind spots relative to repeated sampling from one model?
3. Does interactive debate add value over independent parallel review followed by aggregation?
4. Does explicit evidence-resolution outperform consensus or majority voting?
5. Does a human orchestrator improve adjudication, and under what conditions does human anchoring or confirmation bias offset that benefit?
6. Where do conformity, sycophancy, persuasion, context dilution, problem drift, correlated model errors, and cost set the useful limits of adversarial review?
7. Can a defensible latent or dynamical coordinate describing research-review friction be derived from native process measurements?
8. Only if Question 7 survives native derivation and validation: is there evidence for a critical or optimal regime analogous to a SymC boundary?

Questions 7–8 are explicitly downstream. No chi-like quantity is privileged during initial discovery.

---

## 3. Legacy-claim audit

| Legacy construct / claim | v2 disposition | Reason |
|---|---|---|
| Cognitive Adversarial Friction (CAF) as a useful research-process construct | **KEEP, P0-D** | Worth operationalizing and testing. |
| Epistemic validity is proportional to adversarial friction survived | **DEMOTE TO HYPOTHESIS** | Surviving disagreement is not external verification and can reward persuasive error. |
| Heterogeneous AI systems can expose different weaknesses | **KEEP AS TESTABLE / CONTEXT-DEPENDENT** | Plausible and supported by emerging multi-agent literature, but model errors can remain correlated. |
| Structured antagonism is superior to agreement | **TEST AGAINST BASELINES** | Requires direct comparison with independent review, self-critique, voting, and strong single-agent baselines. |
| Human adaptive orchestration is required for rigorous use | **TEST** | Human arbitration may help, but also introduces anchoring and confirmation bias. |
| \(\chi_{method}=\gamma/(2|\omega|)\) is a scientific process coordinate | **DEMOTE TO HEURISTIC CANDIDATE** | No native dynamical identification has yet earned this mapping. |
| \(\chi_{method}\approx1\) is the productive optimum | **RETIRE AS ESTABLISHED CLAIM** | GOM forbids presuming \(\chi=1\) is an optimum; any optimum must be discovered and independently tested. |
| SymC/AIF development validates Hunting Friction | **HISTORICAL CASE STUDY ONLY** | Shared development lineage is not independent validation. |
| Multi-AI workflow is institution-equivalent rigor | **DO NOT CLAIM** | AI systems can share training data, failure modes, and incentives; external verification remains necessary. |

---

## 4. Project-local scientific guardrails

1. AI agreement never counts as verification.
2. Disagreement volume never counts as epistemic validity by itself.
3. Model heterogeneity never implies statistical or epistemic independence.
4. Human adjudication is a measured process component, not an oracle.
5. A claim must ultimately terminate in ground truth, raw evidence, reproducible computation, reliable external sources, or appropriately qualified human evidence.
6. AIF, SymC, or another product of the same methodology cannot independently validate the methodology that helped produce it.
7. No chi-like coordinate receives scientific status without a native derivation, observable mapping, uncertainty model, and independent falsification.
8. No critical-boundary or optimum claim is allowed because a fitted or normalized quantity happens to equal 1.
9. All failures, unresolved disagreements, abstentions, false alarms, and dead ends are retained.
10. The final engine must be able to return **INSUFFICIENT EVIDENCE**.
11. Model name/version, prompt, system context, tool access, source access, sampling settings, and interaction ordering are provenance variables.
12. The strongest fair simple/native comparator for each frozen task is selected before decisive evaluation.
13. Model-to-model criticism is treated as pre-review pressure testing until the disputed object is independently checked.
14. Any post-result refinement incurs promotion debt and cannot rescue the result that motivated it.

---

## 5. Independent experiment sketch (GOM E1)

This sketch is preserved before using targeted literature to design the detailed protocol.

### 5.1 Experimental factors

Candidate workflow conditions:

- **C0 — Strong single-agent review:** one capable model, strong prompt, same tools and evidence access.
- **C1 — Single-agent self-critique:** answer, critique, revise.
- **C2 — Homogeneous multi-agent review:** multiple instances/samples of the same model with interaction.
- **C3 — Heterogeneous independent review:** different models inspect independently, no communication before aggregation.
- **C4 — Heterogeneous interactive debate:** different models can challenge and respond to one another.
- **C5 — Hunting Friction protocol:** independent first passes; explicit friction-seeking critique; atomic contradiction ledger; evidence-demand step; conflict resolution; refusal state; human adjudication where declared.
- **C6 — Tool-assisted strong baseline:** where appropriate, a strong single model with retrieval/computation/tool use but no multi-agent debate.

No condition is presumed to win.

### 5.2 Testbed families

At least three materially different families should be used:

1. **Known-truth structured tasks:** mathematics, logic, code, data-analysis, or synthetic claims where correctness is directly computable.
2. **Seeded research-review tasks:** manuscript-like passages, methods, analyses, or evidence tables containing controlled flaws of known type and severity.
3. **Evidence-grounded factual/method tasks:** claims resolvable against locked source packets so citation and inference errors can be adjudicated without open-web drift.

Later external/prospective testbeds are required before broad generality claims.

### 5.3 Primary observable families

- error-detection recall;
- error-detection precision;
- correction accuracy;
- false-positive / false-rejection rate;
- calibration and confidence error;
- abstention/refusal appropriateness;
- evidence-grounding rate;
- unresolved contradiction rate;
- conformity flips (correct -> incorrect after interaction);
- corrective flips (incorrect -> correct after interaction);
- pairwise and group error correlation;
- debate/problem drift;
- human adjudication accuracy and effort;
- token, time, and monetary cost;
- reproducibility across model/version/prompt perturbations.

### 5.4 Decisive P0-D falsifiers / negative outcomes

The following are scientifically informative and must be preserved:

- C5 does not outperform a strong single-agent or independent-review baseline.
- Interactive debate performs worse than independent parallel review.
- More friction raises false positives or reduces calibration.
- Model heterogeneity fails to reduce correlated error.
- Human arbitration decreases accuracy or increases anchoring.
- The apparent benefit vanishes after controlling for token budget or tool access.
- No stable low-dimensional process variable supports a chi-like reduction.
- Any apparent optimum shifts materially across task families or model families.

---

## 6. Friction Event Record

Initial discovery will **not** collapse the process into one arbitrary CAF score.

Each contradiction/friction event should instead record, at minimum:

- task / claim ID;
- reviewer/model ID and version;
- independence state at first judgment;
- initial answer and confidence;
- contradiction type: structural / mathematical / inferential / empirical / evidentiary / citation / scope / other;
- claimed severity;
- evidence requested;
- evidence supplied;
- whether the contradiction was resolved;
- resolution route;
- correctness after truth/evidence is opened;
- conformity or corrective flip;
- adjudicator decision where present;
- abstention/refusal;
- token/time cost;
- provenance and ordering.

A scalar, vector, latent-state, or dynamical representation may be proposed only after the multivariate process is characterized.

---

## 7. Function Map

Map the operating interior before seeking a preferred boundary.

Primary axes:

- task family and difficulty;
- baseline model competence;
- model heterogeneity;
- number of reviewers;
- independence before interaction;
- interaction topology;
- number of rounds;
- critique depth;
- evidence availability;
- tool access;
- confidence calibration;
- human orchestration level;
- token/time/cost budget;
- error prevalence and severity.

Questions for the Function Map:

- Which architectures catch which classes of error?
- When does disagreement reveal hidden failure versus generate noise?
- When do independent reviewers converge correctly without debate?
- When does interaction produce genuinely new evidence or reasoning?
- When do several internal review organizations produce equivalent outcomes?
- What information is destroyed by majority vote or scalar scoring?
- Which regions are actually occupied by real research workflows?

---

## 8. Limit Map

Preserve and intentionally probe:

- correlated training-data and reasoning errors;
- model monoculture;
- sycophancy and social conformity;
- persuasive-but-wrong agents;
- judge/model bias;
- majority-wrong cascades;
- problem drift;
- context dilution;
- citation laundering and mutually repeated false sources;
- benchmark contamination / memorization;
- order and role effects;
- vendor/model-version drift;
- stochastic instability;
- human anchoring and confirmation bias;
- shared tool or retrieval failures;
- cost escalation without accuracy gain;
- false-alarm saturation;
- cases where disagreement is irreducible because evidence itself is insufficient.

---

## 9. Initial literature-collision result (GOM E2)

The broad idea that multiple LLM agents can debate, critique, aggregate, or deliberate is established prior art. Recent literature also documents important failure modes.

Initial collision set includes:

- Du et al. (2023), *Improving Factuality and Reasoning in Language Models through Multiagent Debate*, arXiv:2305.14325.
- Liang et al. (2023), *Encouraging Divergent Thinking in Large Language Models through Multi-Agent Debate*, arXiv:2305.19118.
- Smit et al. (2023), *Should we be going MAD? A Look at Multi-Agent Debate Strategies for LLMs*, arXiv:2311.17371.
- Chen et al. (2024), *ReConcile: Round-Table Conference Improves Reasoning via Consensus among Diverse LLMs*, ACL 2024, DOI: 10.18653/v1/2024.acl-long.381.
- Kamoi et al. (2024), *When Can LLMs Actually Correct Their Own Mistakes? A Critical Survey of Self-Correction of LLMs*, TACL, DOI: 10.1162/tacl_a_00713.
- Zhang et al. (2025), *If Multi-Agent Debate is the Answer, What is the Question?*, arXiv:2502.08788.
- Pitre et al. (2025), *Multi-Agent Design: Optimizing Agents with Better Prompts and Topologies*, Findings ACL 2025, DOI: 10.18653/v1/2025.findings-acl.1141.
- Kim et al. (2025), *Correlated Errors in Large Language Models*, arXiv:2506.07962.
- Zhu et al. (2026), *Demystifying Multi-Agent Debate: The Role of Confidence and Diversity*, Findings ACL 2026, DOI: 10.18653/v1/2026.findings-acl.1694.
- Cui et al. (2026), *Free-MAD*, Findings ACL 2026, DOI: 10.18653/v1/2026.findings-acl.1600.
- Becker et al. (2026), *Problem Drift in Multi-Agent Debate*, Findings EACL 2026, DOI: 10.18653/v1/2026.findings-eacl.268.

### Residual novelty question

The candidate contribution is **not** “LLMs can debate.”

The residual question is whether a research-specific adversarial protocol that deliberately separates independent first judgment from interaction, records atomic contradictions, demands external evidence resolution, preserves refusal and unresolved states, measures conformity and drift, and retains a human adjudicator as an auditable component can provide reproducible incremental value over simpler review strategies.

Novelty, if any, attaches only to the residual protocol, measurement architecture, empirical results, failure map, and validated prediction capability.

---

## 10. Comparator architecture

The strongest fair comparator depends on the frozen task, but the candidate comparison set includes:

- strong single-agent review;
- single-agent self-critique;
- self-consistency / repeated sampling;
- independent multi-model ensemble without debate;
- majority or confidence-weighted aggregation;
- representative multi-agent debate;
- tool-assisted single-agent verification.

Before P1, the exact comparator for each frozen claim must be selected and frozen under GOM MFR-05.

No weak comparator is acceptable merely because it makes Hunting Friction look favorable.

---

## 11. P0-D execution sequence

### HF2-D0 — Lineage reconstruction
- recover legacy manuscript, methodology, claims, examples, and cited evidence;
- identify what was observation, conjecture, analogy, and assertion;
- preserve contradictions rather than harmonizing them.

### HF2-D1 — Measurement design
- finalize the Friction Event Record;
- define error taxonomy;
- define confidence/calibration capture;
- define independence and interaction provenance;
- define refusal and unresolved states.

### HF2-D2 — Known-truth benchmark generator
- create controlled tasks and seeded research flaws;
- ensure ground truth is generated independently of the tested reviewers;
- produce negative controls and deliberately ambiguous cases.

### HF2-D3 — Baseline harness
Implement C0–C6 under matched evidence and budget conditions where technically possible.

### HF2-D4 — Function Map
Explore workflow behavior without tuning toward a preferred SymC result.

### HF2-D5 — Limit Map
Adversarially induce conformity, drift, correlated error, judge bias, and cost saturation.

### HF2-D6 — Reduction search
Ask whether the multivariate process supports:
- no useful low-dimensional reduction;
- one or more descriptive latent factors;
- vector/modal organization;
- state-transition dynamics;
- or a justified scalar coordinate.

A chi-like reduction is only one possible outcome.

### HF2-D7 — Comparator qualification
Select strongest task-native baselines before any confirmatory freeze.

### HF2-D8 — P1 candidate registration
Only claims that survive P0-D/P0-Q enter full MFR-14 registration and untouched testing.

---

## 12. Explicit non-claims at project start

This project does not currently establish that:

- more adversarial interaction yields more truth;
- multi-agent systems are intrinsically more rigorous than single agents;
- heterogeneous commercial LLMs constitute independent reviewers;
- human oversight guarantees correctness;
- CAF is a validated scalar quantity;
- \(\chi_{method}\) is a physical or mechanistically identified damping ratio;
- \(\chi_{method}=1\) is an optimum;
- SymC/AIF is an independent validation case;
- the method substitutes for domain experts, peer review, experiment, or reproducible evidence;
- any current workflow is ready for P1 confirmation.

---

## 13. Promotion condition

Hunting Friction v2 remains P0-D until at least:

1. the measurement architecture is stable;
2. known-truth tests show what the protocol does and does not detect;
3. the strongest fair comparator set is established;
4. major failure modes are deliberately tested;
5. any proposed reduction is derived from the observed process rather than imposed;
6. a specific predictive/added-value claim can be frozen;
7. a full MFR-14 record can be completed before untouched evidence is opened.

The project is allowed to conclude that the useful contribution is a **structured multivariate review protocol and failure map with no SymC scalar reduction**. That outcome is scientifically acceptable.
