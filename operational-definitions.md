# Operational Definitions

This document consolidates the rules used in the paper to assign evidence levels, assign claimed outcome levels, calculate the claim-evidence gap, and complete the prospective reporting fields.

## Evidence-level assignment

A study receives the highest level for which it presents direct evaluation of the relevant outcome for the population and context examined. Motivation, anticipated use, deployment status, and study-design labels provide context for interpretation; the level assignment itself follows the outcome measured.

### Level 0: Technical performance

The measured object is the performance of the model, method, or technical task. Typical evidence includes accuracy, F1, calibration, robustness, retrieval quality, benchmark results, or other task-performance measures. Supported conclusions concern the evaluated technical task, dataset, or test conditions.

### Level 1: Output quality

The measured object is a property of system output. Typical evidence includes factuality, clarity, readability, harmfulness, usefulness, uncertainty expression, or expert and user judgments of outputs. Human participants may provide these judgments while the measured outcome remains an output property.

### Level 2: User outcome

The measured object is an outcome for a user performing a task. Typical measures include comprehension, task completion, usability, time, confidence, error recovery, or accessibility in a controlled or realistic task. The supported conclusion is scoped to the evaluated population, task, and setting.

### Level 3: Decision or behavior

The measured object is a meaningful decision or action by the relevant actor, including users, practitioners, moderators, teachers, clinicians, caseworkers, or other institutional actors. Participation by these actors reaches Level 3 when the study directly measures the consequential decision or behavior.

### Level 4: Operational outcome

The measured object is an organizational, workflow, or service outcome such as processing time, workload, service uptake, referral completion, institutional response, or another operational indicator. Deployment supplies the setting; Level 4 classification follows direct measurement of the operational outcome.

### Level 5: Social outcome

The measured object is a population or community outcome such as health, learning, safety, inclusion, welfare, equity, an environmental outcome, or another appropriate social outcome. The field design should be appropriate to the outcome and causal question, while the level assignment continues to follow the outcome measured.

## Claimed outcome level

C is the highest SOLIAS outcome level presented as a result in the title, abstract, interpretation, discussion, or conclusion. Statements of motivation and intended use can refer to broader outcomes when their prospective status is clear. Expressions such as "may support," "is intended to support," and "is a component of" can be used for that purpose. Statements such as "improves access," "reduces harm," or "improves health" are assigned to the corresponding claimed outcome level when the paper presents them as study results.

## Claim-evidence gap

`G = max(0, C - E)`

G records the number of additional outcome transitions represented in the claim. The complete `(E, C, G)` profile should be retained because methodological quality, causal validity, population fit, equity, safety, and ethical appropriateness are assessed within the relevant outcome layer and cannot be inferred from G alone.

## Checklist response rule

Checklist responses may be concise and may cite manuscript pages where the information already appears. An item may be designated not applicable when the response gives the reason. The [complete checklist](checklist/solias-checklist.md) provides the minimum useful response for each item.

## Evidence-calibrated conclusion

An evidence-calibrated conclusion states the demonstrated outcome for the evaluated population and context, identifies broader intended outcomes as prospective, and names the next evaluation target when the research program extends beyond the outcome measured in the current study.
