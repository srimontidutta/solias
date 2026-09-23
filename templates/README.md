# SOLIAS Templates

The repository provides human-readable forms and machine-readable starting points for the main SOLIAS workflows.

| Task | Template |
| --- | --- |
| Complete the full prospective checklist | [`author-form.md`](author-form.md) or [`author-form.csv`](author-form.csv) |
| Apply SOLIAS during peer review | [`reviewer-form.md`](reviewer-form.md) |
| Use the compact venue fields | [`short-form.md`](short-form.md) or [`short-form.csv`](short-form.csv) |
| Record only `(E, C, G)` in JSON | [`claim-evidence-profile.template.json`](claim-evidence-profile.template.json) |
| Record only `(E, C, G)` in YAML | [`claim-evidence-profile.template.yaml`](claim-evidence-profile.template.yaml) |
| Prepare a complete machine-readable report in JSON | [`solias-report.template.json`](solias-report.template.json) |
| Prepare a complete machine-readable report in YAML | [`solias-report.template.yaml`](solias-report.template.yaml) |

The JSON and YAML machine-readable templates leave required substantive fields as `null`. Validation is intended after those fields have been completed. This preserves an unassigned starting state for evidence levels, claim levels, applicability judgments, and reporting statuses.

Completed machine-readable examples are provided under [`../schema/`](../schema/) so that a filled record can be compared with the blank templates before validation.
