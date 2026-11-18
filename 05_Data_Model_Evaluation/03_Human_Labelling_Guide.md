# Human Labelling Guide

## Objective

Human labels provide the reference against which RiskReview AI findings are evaluated. Labels must be created by reviewers who understand the relevant automotive, wind-energy, cybersecurity, data, governance, or commercial context.

## Labelling Unit

The labelling unit is one risk record plus its available evidence. Reviewers label individual findings, not only the record as a whole.

## Labels

| Label | Meaning |
|---|---|
| `Correct` | The finding is supported and useful without material change |
| `Partially Correct` | The finding is directionally useful but requires modification |
| `Incorrect` | The finding is unsupported, misleading, or irrelevant |
| `Insufficient Evidence` | The reviewer cannot decide from the available evidence |
| `Not Applicable` | The check does not apply to the record |

## Finding Types

- Missing mandatory information
- Weak cause-event-impact structure
- Missing or stale evidence
- Related or duplicate risk
- Model or data drift concern
- Supplier transparency gap
- Cybersecurity or update-integrity concern
- Responsible AI or fairness concern
- Explainability limitation
- Human-approval or governance gap
- Financial-assumption or projection concern

## Labelling Procedure

1. Read the risk record without viewing the model finding.
2. Review the evidence reference and intended-use context.
3. Record the expected finding and reason.
4. View the model finding.
5. Assign a label.
6. Record any required correction.
7. Identify the potential consequence of accepting an incorrect finding or missing a correct finding.
8. Escalate unresolved domain questions.

## Severity of Evaluation Error

| Error Severity | Description | Example |
|---|---|---|
| Critical | Could support an unsafe or unauthorised launch or commissioning decision | Missing a Critical control or approval gap |
| High | Could conceal significant model, cyber, supplier, or operational exposure | Missing material drift or update-integrity risk |
| Medium | Causes avoidable rework or weakens evidence quality | Incorrect related-risk suggestion |
| Low | Minor wording or presentation issue | Non-material phrasing difference |

## Multiple Reviewers

Critical and High test cases should be independently labelled by at least two qualified reviewers. Disagreements should be resolved through documented adjudication by a designated domain or governance reviewer.

## Reviewer Record

Capture:

- Reviewer role
- Review date
- Record and finding identifier
- Initial label
- Reason
- Corrected finding, if required
- Adjudicated label
- Adjudicator role

## Bias Controls

- Mix automotive, wind-energy, and cross-enterprise records.
- Include positive and negative cases.
- Hide expected labels from the model.
- Avoid using only records written in one style.
- Review performance separately by domain and finding type.
- Do not treat reviewer agreement as proof that the underlying risk score is objectively correct.
