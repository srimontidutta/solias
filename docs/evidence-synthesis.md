# Use in Evidence Synthesis

SOLIAS can organize a body of literature according to the outcome each study directly demonstrates. This representation is useful when papers share a broad social motivation but evaluate different points along the outcome pathway.

## Core extraction

For each study, record:

- the intended outcome;
- E, the highest outcome directly evaluated;
- C, the highest outcome presented as a result;
- G, calculated as `max(0, C - E)`;
- the population and context supporting E; and
- the reporting fields needed to interpret the mechanism, evaluation, responsible-operation conditions, and scope of the conclusion.

A [retrospective paper-extraction schema](../schema/retrospective/paper-extraction.schema.json) is provided for structured use.

## Interpretation

Studies can then be grouped by demonstrated outcome. Technical studies contribute evidence about model or task performance, user studies can contribute evidence about task success or comprehension, and operational studies can contribute evidence about service or workflow outcomes. The resulting synthesis retains the outcome transitions that connect these contributions within a broader research program.

The claim-evidence profile also identifies transitions for which direct evidence remains limited. Those transitions describe the relationship between the evidence reported in a study and the outcome presented in its conclusion; explanations for why particular claims were made require separate analysis of the study and its context.
