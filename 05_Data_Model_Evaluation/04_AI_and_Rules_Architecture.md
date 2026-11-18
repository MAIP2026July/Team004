# AI and Rules Architecture

## Architecture Principle

RiskReview AI combines deterministic rules, model-assisted analysis, human review, governance gates, and auditable monitoring. Deterministic checks are used where requirements are explicit. AI is used where language, similarity, evidence, or operational patterns require contextual analysis.

## Processing Flow

1. **Input layer** receives a CSV, workbook, system record, or approved monitoring event.
2. **Schema and validation layer** checks required fields, types, dates, value ranges, and formula consistency.
3. **Rules engine** checks overdue actions, score thresholds, missing evidence, approval requirements, and governance gates.
4. **AI analysis layer** reviews cause-event-impact structure, evidence relevance, related risks, supplier transparency, explanation limitations, and monitoring signals.
5. **Explanation layer** returns the finding, evidence, model or rule version, uncertainty, limitations, and proposed next action.
6. **Human review layer** supports accept, reject, modify, request-evidence, link, merge, defer, or escalate decisions.
7. **Governance layer** applies approved scores, risk tiers, segregation of duties, and launch or commissioning gates.
8. **Audit and monitoring layer** records decisions and watches model, data, fairness, security, supplier, and operational changes.

## Rules and AI Allocation

| Capability | Rules | AI Model | Human |
|---|---:|---:|---:|
| Mandatory-field validation | Yes | No | Correct or approve exception |
| Date and score-range validation | Yes | No | Correct or approve exception |
| Inherent and residual score calculation | Yes | No | Approve inputs |
| Cause-event-impact quality review | Partial | Yes | Confirm or edit finding |
| Evidence relevance and freshness | Partial | Yes | Verify evidence |
| Related-risk suggestion | No | Yes | Link, merge, or reject |
| Drift and anomaly detection | Threshold support | Yes | Investigate and decide action |
| Risk acceptance | No | No | Required |
| Launch or commissioning decision | Gate support | No | Required |

## Model Inputs

- Risk text and category
- Human owner and workflow status
- Evidence metadata and approved content
- Model, dataset, software, hardware, and supplier version
- Monitoring metrics and incidents
- Intended-use and prohibited-use information

## Model Outputs

- Finding type
- Finding statement
- Evidence reference
- Rationale
- Uncertainty or confidence information
- Known limitation
- Suggested next action
- Model and prompt version

## Security and Privacy

- Apply least-privilege access.
- Encrypt data in transit and at rest.
- Separate customer or programme data by approved boundary.
- Do not send confidential evidence to unapproved external models.
- Minimise personal and proprietary data.
- Log model and human access to material records.
- Retain and delete records according to the approved policy.

## Failure Handling

- Invalid input is rejected with field-level errors.
- Missing evidence produces an evidence-gap finding, not an invented conclusion.
- Unsupported model output is rejected or escalated by the reviewer.
- Model service failure falls back to deterministic checks and human review.
- Material version change triggers revalidation.
- Critical and unresolved High risks remain blocked or restricted until authorised review.
