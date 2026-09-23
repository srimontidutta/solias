# SOLIAS Reporting Standard

## Status

This repository specification accompanies the pre-publication release of *SOLIAS: A Reporting Standard for Social-Impact Claims in NLP*. The definitions, evidence-level ontology, claim-evidence representation, checklist, examples, reviewer sequence, and governance provisions follow the paper.

## 1. Scope

SOLIAS applies to research that connects an NLP contribution to an outcome for people, institutions, or communities. The reporting object is the relationship among the intended outcome that motivates the work, the demonstrated outcome directly evaluated in the study, and the claimed outcome presented as a result. Outcome selection, measurement, study design, causal method, and domain-specific safeguards remain matters for the relevant research setting and methodological community.

## 2. Evidence-calibration rule

A social-impact claim is evidence-calibrated when it reflects the highest outcome layer directly evaluated for the relevant population and context and clearly distinguishes demonstrated outcomes from intended ones.

## 3. Core terms

**Intended outcome.** The longer-term objective that motivates the research program.

**Demonstrated outcome.** The highest outcome layer directly evaluated for the population and context examined.

**Claimed outcome.** The highest outcome layer that the paper presents as a result in its title, abstract, interpretation, discussion, or conclusion.

**Evidence level (E).** The SOLIAS level assigned to the demonstrated outcome.

**Claimed outcome level (C).** The SOLIAS level assigned to the claimed outcome.

**Claim-evidence gap (G).** The number of additional outcome transitions represented in the claim, calculated as `G = max(0, C - E)`.

## 4. Evidence levels

| Level | Outcome | Direct evidence may include | Scope of supported conclusion |
| ---: | --- | --- | --- |
| 0 | Technical performance | Accuracy, F1, calibration, robustness, retrieval quality, benchmark results, or performance on a stated technical task | System or method performance on the evaluated technical task, dataset, or test conditions |
| 1 | Output quality | Factuality, clarity, readability, harmfulness, usefulness, uncertainty expression, or expert and user judgments of outputs | Measured properties of system outputs under the stated evaluation conditions |
| 2 | User outcome | Comprehension, task completion, usability, time, confidence, error recovery, or accessibility in a controlled or realistic task | Measured user outcome for the evaluated population, task, and setting |
| 3 | Decision or behavior | Observed decisions or actions by users, practitioners, moderators, teachers, clinicians, caseworkers, or other institutional actors | Measured decision or behavioral outcome in the evaluated context |
| 4 | Operational outcome | Workflow performance, service uptake, referral completion, processing time, workload, institutional response, or deployment indicators | Measured operational or service outcome in the evaluated organization or setting |
| 5 | Social outcome | Health, learning, safety, inclusion, welfare, equity, environmental, or other population outcomes measured through an appropriate field design | Measured social outcome for the defined population and context |

A study receives the highest level for which it directly evaluates the corresponding outcome for the relevant population and context. The level identifies what was measured, while methodological appraisal addresses the credibility, validity, and scope of the evidence at that level.

## 5. Assignment rules

Level assignment follows the measured outcome, so human participation can occur at several levels: judgments of output factuality or clarity provide Level 1 evidence, while measured comprehension or task success provides Level 2 evidence. A consequential decision or action provides Level 3 evidence when that decision or action is measured directly. Operational measures such as processing time, workload, service uptake, referral completion, or institutional response provide Level 4 evidence. Level 5 is assigned when the study measures the relevant social outcome for the defined population and context.

Deployment and study design contribute to the interpretation and credibility of the evidence. The evidence level itself continues to follow the outcome measured. The representative adjacent-level cases from the paper are reproduced in [examples/boundary-cases.md](examples/boundary-cases.md).

## 6. Claim-evidence profile

A SOLIAS report records `(E, C, G)` using the same six-level ontology for demonstrated and claimed outcomes:

```text
E = highest outcome level directly evaluated
C = highest outcome level presented as a result
G = max(0, C - E)
```

When `G = 0`, the highest claimed outcome is at or below the outcome directly evaluated. Positive values record the additional outcome transitions represented in the claim. Interpretation uses the complete profile because equal values of G can connect different outcome layers and therefore different forms of evidence.

Construct validity, realism, population fit, uncertainty, safety, causal strength, and other methodological considerations are assessed within the demonstrated level and remain separate from the ordinal gap.

## 7. Checklist

The prospective SOLIAS checklist contains 20 items organized into six reporting functions.

**Purpose and population:** social problem; target population; excluded or at-risk groups; intended outcome; stakeholders.

**System and pathway:** NLP function; use context; theory of change.

**Evidence and alignment:** demonstrated evidence level; claimed outcome level and gap; evaluation measures.

**Outcome evaluation:** output quality; user outcome; decision or behavior; operational outcome; social outcome.

**Responsible operation:** equity and accessibility; safety and failure-to-harm; maintenance and monitoring.

**Calibrated conclusion:** evidence-calibrated conclusion.

The [complete checklist](checklist/solias-checklist.md) gives the reporting question and minimum useful response for each item. Responses may be concise, manuscript page references may be used where appropriate, and an item may be designated not applicable when the justification is stated.

## 8. Evidence-calibrated conclusions

The paper provides the following flexible claim template:

> For [population] in [context], the system provides [NLP function]. In [evaluation], it changed [measured outcome] relative to [comparison], providing SOLIAS Level [E] evidence. The system is intended to contribute to [broader outcome], which requires evaluation of [next outcome] in [next setting].

The template places the measured result and the broader research objective in the same account while keeping their evidentiary status explicit.

## 9. Author use

During study design, authors can identify the intended outcome, target population, use context, theory of change, and highest outcome the planned study will directly measure. During manuscript preparation, they assign `(E, C, G)`, complete the checklist, and state the demonstrated outcome separately from broader intended outcomes. When `C > E`, the paper describes three available responses: evaluation of a missing transition, calibration of the conclusion to the demonstrated outcome, or identification of the broader outcome as a subsequent evaluation target.

## 10. Reviewer use

Reviewers identify E, assess methodological quality within that level, identify C, report `(E, C, G)`, and use the checklist to interpret the claim in its population and context. A bounded technical contribution can therefore be assessed on the quality of its technical evidence while a broader social objective remains prospective. The [reviewer form](templates/reviewer-form.md) reproduces the six-step sequence from the paper.

## 11. Venue use

A venue may request a short form containing `(E, C, G)`, the relevant population and context, the theory of change, and an evidence-calibrated conclusion. The [venue-adoption guide](docs/venue-adoption.md) provides copy-ready wording derived from the paper.

## 12. Machine-readable representation

The repository provides a standalone schema for the `(E, C, G)` profile and a full schema for prospective SOLIAS reports. Both use JSON Schema Draft 2020-12, with YAML serializations supplied for readers who work in YAML. The profile schema validates the full set of permitted `(E, C, G)` combinations, including the arithmetic relation `G = max(0, C - E)`. The full-report schema applies the same rule within a complete record.

Blank JSON and YAML templates leave required values unset and are intended to be filled before validation. A completed synthetic report from the paper is supplied as a validation example.

## 13. Retrospective extraction

Retrospective coding serves evidence synthesis and historical analysis, whereas the prospective checklist supports authors and reviewers preparing new work. The [retrospective extraction schema](schema/retrospective/paper-extraction.schema.json) records demonstrated evidence, claimed outcome, gap, supporting references, and the observable reporting components described in the paper's retrospective crosswalk.

## 14. Domain profiles

Domain profiles may add examples, recommended measures, safeguards, and implementation guidance for a particular setting. The six evidence levels and `(E, C, G)` representation remain common across profiles so that studies can retain a shared outcome classification while domain specialists define appropriate measures and methods.

## 15. Versioning and governance

Major revisions to the evidence-level ontology or `(E, C, G)` representation increment the major version. Compatible clarifications, implementation guidance, and domain-specific examples may increment minor versions. Proposed changes are documented through the public issue log described in [GOVERNANCE.md](GOVERNANCE.md).
