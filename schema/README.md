# SOLIAS Machine-Readable Schemas

The schema directory separates the compact claim-evidence profile from the complete prospective report and from retrospective literature extraction. This makes it possible to adopt only the representation needed for a particular workflow.

## Which file should I use?

| Use | Schema | Blank template | Completed example |
| --- | --- | --- | --- |
| Record only `(E, C, G)` | [`claim-evidence-profile.schema.json`](claim-evidence-profile.schema.json) | [`claim-evidence-profile.template.json`](../templates/claim-evidence-profile.template.json) or [`claim-evidence-profile.template.yaml`](../templates/claim-evidence-profile.template.yaml) | Any row in [`../data/claim-evidence-profiles.csv`](../data/claim-evidence-profiles.csv) |
| Record a complete prospective SOLIAS report | [`solias-report.schema.json`](solias-report.schema.json) | [`solias-report.template.json`](../templates/solias-report.template.json) or [`solias-report.template.yaml`](../templates/solias-report.template.yaml) | [`example-report.json`](example-report.json) or [`example-report.yaml`](example-report.yaml) |
| Extract SOLIAS fields from published papers | [`retrospective/paper-extraction.schema.json`](retrospective/paper-extraction.schema.json) | Create records from the fields in the schema | See [evidence-synthesis guidance](../docs/evidence-synthesis.md) |

## Claim-evidence profile schema

The standalone profile schema contains `E`, `C`, and `G` as integers from 0 through 5. Its permitted combinations encode `G = max(0, C - E)`, so a record with an inconsistent gap fails validation.

The JSON and YAML schema files are equivalent serializations of the same Draft 2020-12 schema. The CSV table under `data/` lists every valid profile for spreadsheet and manual use.

## Full prospective report schema

`solias-report.schema.json` represents the prospective SOLIAS checklist in a grouped structure that follows the six reporting functions used in the paper. The record includes:

- purpose and population;
- system and pathway;
- the validated `(E, C, G)` profile;
- demonstrated evidence and the claim presented as a result;
- evaluation measures;
- output, user, decision, operational, and social outcome fields;
- equity and accessibility, safety and failure-to-harm, and maintenance and monitoring; and
- the evidence-calibrated conclusion.

The full schema also enforces the permitted `(E, C, G)` combinations. Strings required in a completed report have a minimum length of one character. Outcome-evaluation fields distinguish `evaluated`, `not_evaluated`, and `not_applicable`, while responsible-operation fields distinguish `addressed`, `not_addressed`, and `not_applicable`. In either case, `not_applicable` should be accompanied by the reason in the response field.

## Blank templates

The blank templates use `null` for fields that require completion. They are intentionally invalid until the required values have been supplied. This prevents a copied template from being mistaken for a completed SOLIAS report and avoids pre-populating substantive judgments such as an evidence level or applicability status.

## Completed example

`example-report.json` and `example-report.yaml` reproduce the synthetic disaster-response example from the paper in machine-readable form. The JSON example validates against `solias-report.schema.json`.

## Retrospective extraction

The schema under `retrospective/` supports literature review and evidence synthesis. It uses the same validated `(E, C, G)` profile as the prospective representation and adds source references plus the observable reporting components used for historical papers. The prospective report schema remains the appropriate representation for authors completing SOLIAS on new work.
