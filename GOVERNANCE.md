# SOLIAS Governance

The governance process follows the release and governance plan described in the paper. It is intended to keep the common classification stable while allowing implementation guidance and domain-specific practice to develop through documented revision.

## Release package

The SOLIAS release package includes a versioned author form, reviewer form, machine-readable schema, operational definitions, worked examples, and a public issue log. Proposals for change should identify the affected item, the empirical or conceptual rationale, and the compatibility implications for previously completed forms and machine-readable records.

## Public issue log

Repository issues are organized into four categories corresponding to the governance plan:

- **Clarification request:** interpretation of an existing definition, checklist item, schema field, or example;
- **Implementation problem:** difficulty applying the standard, forms, or schema in practice;
- **Domain profile proposal:** additional examples, measures, safeguards, or implementation guidance for a particular setting; and
- **Core classification change:** a proposed revision to the evidence-level ontology, `(E, C, G)` representation, or another part of the common classification.

The issue forms in `.github/ISSUE_TEMPLATE/` collect the information needed for review.

## Versioning

Major revisions to the evidence-level ontology or `(E, C, G)` representation increment the major version. Compatible clarifications, implementation guidance, and domain-specific examples may increment minor versions. Deprecated fields or definitions remain documented together with migration guidance for previously completed forms and machine-readable records.

## Domain profiles

Domain-specific extensions are released as profiles that may provide examples, recommended measures, safeguards, or implementation guidance for settings such as healthcare, education, and public services while preserving the meanings of the six evidence levels and `(E, C, G)`.

## Review of substantive changes

For substantive revisions, maintainers record the proposal, supporting evidence, stakeholder feedback, final decision, and effective version. Governance decisions draw on documented evidence from implementation and use.

Prospective development should involve researchers across application settings, practitioners, affected communities, research-methods experts, venue leadership, reviewers, and authors. Evaluation of the standard should examine completion time, inter-rater agreement, effects on claim wording and study design, usability in peer review and evidence synthesis, and possible unintended incentives. Domain-profile development should also examine whether proposed outcomes, measures, safeguards, and reporting criteria reflect the priorities and conditions of the populations represented.
