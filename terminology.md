# SOLIAS Terminology

This glossary collects the terms used across the SOLIAS paper, specification, checklist, templates, and machine-readable schemas.

## Social-impact claim

A claim connecting an NLP contribution to an outcome for people, institutions, or communities. SOLIAS uses this relationship as its primary reporting object.

## Intended outcome

The longer-term objective that motivates the research program. An individual study may locate this outcome later in the research program than the outcome it directly evaluates.

## Demonstrated outcome

The highest outcome layer directly evaluated for the population and context examined.

## Claimed outcome

The highest outcome layer presented as a result in the title, abstract, interpretation, discussion, or conclusion. Motivation and intended use can refer to broader prospective outcomes while the claimed outcome level continues to follow the outcome presented as a result.

## Evidence-calibrated claim

A claim that reflects the highest outcome layer directly evaluated for the relevant population and context and clearly distinguishes demonstrated outcomes from intended ones.

## Evidence level (E)

The level corresponding to the highest outcome directly evaluated. SOLIAS uses six levels: technical performance (L0), output quality (L1), user outcome (L2), decision or behavior (L3), operational outcome (L4), and social outcome (L5).

## Claimed outcome level (C)

The level corresponding to the highest outcome presented as a result, using the same six-level ontology as E.

## Claim-evidence gap (G)

The ordinal distance between the demonstrated and claimed outcome levels when the claim extends beyond the demonstrated outcome:

`G = max(0, C - E)`

## Claim-evidence profile

The claim-evidence profile is the tuple `(E, C, G)`, reported in full so that both outcome levels remain visible together with their gap. This supports interpretation of studies that have the same G but evaluate different outcomes.

## Theory of change

An account of how the NLP function is expected to contribute to the intended outcome, including intermediate user actions, institutional responses, assumptions, and dependencies appropriate to the setting.

## Outcome pathway

The reporting scaffold that places technical performance, output quality, user outcomes, decisions or behavior, operational outcomes, and social outcomes along the pathway connecting a language system to broader consequences. It identifies the outcome directly observed and the additional transitions represented in a broader claim while allowing the causal structure of a particular application to remain domain-specific.

## Domain profile

A domain-specific extension that adds examples, recommended measures, safeguards, or implementation guidance while preserving the meanings of the six evidence levels and the `(E, C, G)` representation.
