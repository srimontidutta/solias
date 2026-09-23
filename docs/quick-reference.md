# SOLIAS Quick Reference

## Evidence-calibration rule

A social-impact claim is evidence-calibrated when it reflects the highest outcome layer directly evaluated for the relevant population and context and clearly distinguishes demonstrated outcomes from intended ones.

## Six evidence levels

| Level | Outcome | Typical measured object |
| ---: | --- | --- |
| L0 | Technical performance | Model or task performance |
| L1 | Output quality | Properties of generated, retrieved, or classified outputs |
| L2 | User outcome | Task success, comprehension, usability, time, accessibility |
| L3 | Decision or behavior | Observed action or decision by a relevant actor |
| L4 | Operational outcome | Workflow, service, uptake, workload, institutional response |
| L5 | Social outcome | Population or community outcome |

## Claim-evidence profile

```text
E = highest outcome level directly evaluated
C = highest outcome level presented as a result
G = max(0, C - E)
```

Report the complete `(E, C, G)` profile so that the demonstrated and claimed outcome layers remain visible together with their gap.

## Five questions for a social-impact claim

1. What broader outcome motivates the work?
2. What outcome was directly measured for the relevant population and context?
3. What is the highest outcome presented as a result?
4. Which outcome transitions remain unevaluated?
5. What population, context, mechanism, safeguards, and maintenance conditions are needed to interpret the claim?

## Flexible claim template

> For [population] in [context], the system provides [NLP function]. In [evaluation], it changed [measured outcome] relative to [comparison], providing SOLIAS Level [E] evidence. The system is intended to contribute to [broader outcome], which requires evaluation of [next outcome] in [next setting].

## Boundary reminders

- Human judgments of output properties correspond to Level 1 when the output remains the measured object.
- Measured task success or comprehension corresponds to Level 2.
- A directly measured consequential decision or action corresponds to Level 3.
- Operational measures such as processing time, workload, service uptake, referral completion, or institutional response correspond to Level 4.
- Level 5 corresponds to direct measurement of the relevant population or community outcome for the defined population and context.
