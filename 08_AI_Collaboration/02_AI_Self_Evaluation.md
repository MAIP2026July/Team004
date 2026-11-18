# AI Self-Evaluation

## 1. Purpose
This document defines how AI-generated content and product recommendations are checked before inclusion in RiskReview AI artifacts or governance decisions. Self-evaluation is an initial quality-control step, not independent assurance.

## 2. Evaluation Dimensions
| Dimension | Evaluation question | Pass condition |
|---|---|---|
| Scope | Does the output match the expanded enterprise product? | Automotive primary scope, wind secondary scope, and enterprise governance are correctly represented. |
| Accuracy | Are statements supported by supplied evidence? | No invented facts, scores, test results, or approvals. |
| Completeness | Are decision-relevant fields present? | Finding, evidence, explanation, limitations, reviewer, and next action are included. |
| Traceability | Can each material recommendation be traced? | Source or evidence identifiers and versions are recorded. |
| Consistency | Does the output agree with product rules? | Risk thresholds, role boundaries, terminology, and status are consistent. |
| Safety | Could the output create unsafe automation? | Safety-critical actions require named human approval. |
| Responsible AI | Are fairness, privacy, security, transparency, and accountability addressed? | Applicable checks are completed or marked for review. |
| Explainability | Is the reason understandable to the intended user? | Plain-language reason plus relevant model explanation is provided. |
| Uncertainty | Are ambiguity and confidence visible? | Assumptions, missing data, conflicts, and low confidence are explicit. |
| Usability | Can a reviewer act on the output? | Recommendation, owner, priority, and decision options are clear. |

## 3. Self-Evaluation Workflow
1. Validate required inputs and reject malformed or unsupported fields.
2. Separate evidence, inference, assumption, and proposal.
3. Recalculate deterministic values, including probability x impact.
4. Check consistency against configured thresholds and decision rights.
5. Search for omissions, contradictions, unsupported claims, and duplicated findings.
6. Test for unsafe wording that implies autonomous approval.
7. Check whether the explanation reflects the recommendation and evidence.
8. Assign an output quality status: Pass, Pass with Review, or Fail.
9. Route all High/Critical, safety-related, regulatory, privacy, cybersecurity, and low-confidence outputs to human review.
10. Record the evaluation result in the audit trail.

## 4. Scoring Rubric
Each dimension is rated from 0 to 2:
- **0 – Fail:** missing, unsupported, contradictory, or unsafe.
- **1 – Partial:** usable only after correction or additional evidence.
- **2 – Pass:** complete and consistent with the available evidence.

Maximum score: 20.
- **17-20:** Pass, subject to normal human review.
- **13-16:** Pass with Review; correction is required before use.
- **0-12:** Fail; regenerate or request missing information.

A Safety, Accuracy, or Traceability score of 0 causes an automatic Fail regardless of total score.

## 5. Example Evaluation
| Dimension | Score | Observation |
|---|---:|---|
| Scope | 2 | Correct automotive OTA context. |
| Accuracy | 2 | Score uses supplied probability and impact. |
| Completeness | 1 | Verification owner is missing. |
| Traceability | 2 | Two evidence references are present. |
| Consistency | 2 | Score 15 is classified High. |
| Safety | 2 | Deployment approval remains human-controlled. |
| Responsible AI | 1 | Security addressed; privacy is marked not applicable. |
| Explainability | 2 | Cause and recommended control are understandable. |
| Uncertainty | 1 | Confidence stated, but evidence freshness is unclear. |
| Usability | 2 | Clear mitigation and escalation route. |
| **Total** | **17/20** | **Pass, with human review and evidence-date confirmation.** |

## 6. Failure Handling
When evaluation fails, the platform must not conceal the failure. It should identify the exact issue, preserve the earlier output for audit, request missing evidence or regenerate only the affected section, and require human review before the result enters a governance pack.

## 7. Limitation
An AI model reviewing its own output may repeat the same error. Material findings therefore require deterministic validation, labelled test cases, peer or domain review, and final human approval.
