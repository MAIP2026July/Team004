# Data Strategy

## Scope
RiskReview AI initially supports monthly programme-risk and launch-readiness reviews for Tier 1 and Tier 2 automotive component manufacturers conducting NPD/NPI programmes from APQP to Start of Production.

## Input data
The prototype uses fictional records containing risk ID, programme, APQP phase, workstream, cause, uncertain event, impact, owner, mitigation, action owner, due date, review date, evidence reference, evidence date and status.

## Data boundaries
- Synthetic data only for the prototype.
- No customer drawings, supplier quotations, employee data or confidential programme records.
- No automatic probability, impact, FMEA, PPAP or Start-of-Production decisions.
- Human reviewers confirm every AI-assisted finding.

## Dataset plan
Create at least 60 fictional records covering strong and weak statements, true and false related-risk pairs, aligned and weak mitigations, missing fields, overdue actions and stale evidence.

## Split
- Development: 60%
- Validation: 20%
- Held-out evaluation: 20%

Related-risk pairs must be split by programme context to reduce leakage.

## Governance
Version the dataset, schema, labels, rules, prompts and evaluation results. Record who changed each item and why.
