# RiskReview AI Product Risk Register

## Scoring Method

Each risk is assessed using:

- **Likelihood:** 1 Rare to 5 Almost certain
- **Impact:** 1 Negligible to 5 Severe
- **Priority score:** Likelihood multiplied by impact

Scores are provisional product-management assessments, not validated organisational risk ratings.

| ID | Risk | Potential harm | Likelihood | Impact | Score | Preventive control | Detection and response | Owner |
|---|---|---|---:|---:|---:|---|---|---|
| RAI-01 | AI fabricates programme facts | Incorrect review decisions and loss of trust | 3 | 5 | 15 | Ground findings in supplied text; prohibit unsupported new facts | Human review, unsupported-fact sampling, incident logging | Product Manager |
| RAI-02 | Suggested rewrite changes risk meaning | Cause, event or impact is misunderstood | 3 | 5 | 15 | Side-by-side comparison; meaning-preservation check | Mandatory confirmation; rollback to original text | NPD Project Manager |
| RAI-03 | Distinct risks are incorrectly suggested as duplicates | A material risk may be hidden or merged | 3 | 5 | 15 | Related-risk wording instead of automatic duplicate claim | Human compare, link, merge or keep separate | APQP Coordinator |
| RAI-04 | Writing-style bias | Some workstreams or users receive more negative findings | 3 | 4 | 12 | Diverse synthetic examples and style-neutral rubric | Segment-level evaluation and reviewer feedback | Evaluation Lead |
| RAI-05 | Confidential programme data is exposed | Customer, supplier or launch information is disclosed | 2 | 5 | 10 | Synthetic data only for prototype; access control for pilot | Access log review and incident response | Data Owner |
| RAI-06 | Users over-trust AI output | Weak recommendations become official decisions | 3 | 5 | Advisory labels, uncertainty, required human action | Monitor acceptance without review; user training | Product Manager |
| RAI-07 | Model or provider behaviour changes | Quality degrades without visible code changes | 3 | 4 | Version pinning where possible; regression suite | Scheduled evaluation; provider fallback | Technical Lead |
| RAI-08 | Required evidence is stale or incorrectly interpreted | Review agenda prioritises the wrong item | 3 | 4 | Configurable evidence-age rules and source display | Human verification and correction | APQP Coordinator |
| RAI-09 | Poor synthetic data creates misleading evaluation | Prototype appears stronger than it is | 4 | 4 | Independent labelling and challenge cases | Held-out set and disagreement review | Team004 |
| RAI-10 | Manual review workload is too high | Product creates more work than it removes | 3 | 3 | Prioritised queue and limited MVP findings | Measure time per risk and correction burden | Product Manager |
| RAI-11 | Rules are configured incorrectly | Valid records are flagged or invalid records pass | 2 | 4 | Rule tests and customer-approved configuration | Rules-only test suite and audit log | Technical Lead |
| RAI-12 | Product is confused with FMEA or PPAP approval | Governance misuse and incorrect reliance | 3 | 5 | Explicit scope boundaries throughout UI and documentation | Training, prohibited-use checks and audit review | Product Manager |
| RAI-13 | Integration writes unverified changes | Official register is altered prematurely | 2 | 5 | Prototype is read-only; production uses approval gate | Change log and rollback | System Owner |
| RAI-14 | Commercial claims exceed evidence | Buyer is misled about value or performance | 3 | 4 | Label assumptions and provisional measures | Review external claims against measured evidence | Business Owner |

## Review Cadence

- Prototype stage: review after each major build
- Controlled pilot: weekly review
- Production candidate: monthly governance review and after every material change
- Severe incident: immediate review

## Escalation

Any risk with an impact score of 5, or an observed priority score of 15 or above, must be reviewed before the next release decision.
