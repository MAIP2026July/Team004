# Metrics and Thresholds

## Classification Metrics

| Metric | Formula or Meaning | Initial Academic Target |
|---|---|---|
| Precision | True positives ÷ all positive findings | ≥ 0.80 overall |
| Recall | True positives ÷ all required findings | ≥ 0.85 overall |
| F1 Score | Harmonic mean of precision and recall | ≥ 0.82 overall |
| Critical/High Recall | Recall for Critical and High findings | ≥ 0.95 |
| False Negative Rate | Missed required findings ÷ all required findings | ≤ 0.05 for Critical/High |
| False Positive Rate | Incorrect alerts ÷ all negative cases | ≤ 0.15 overall |

Targets are proposed acceptance thresholds, not achieved results.

## Human-Review Metrics

| Metric | Initial Target |
|---|---|
| Material findings receiving human disposition | 100% |
| Critical and High decisions with recorded justification | 100% |
| Decisions with retrievable evidence and versions | 100% |
| Unauthorised autonomous launch or commissioning decisions | 0 |
| Critical overrides with named approval and review date | 100% |

## Explanation Metrics

- Reviewer can identify the model finding.
- Reviewer can locate supporting evidence.
- Reviewer can state at least one limitation.
- Reviewer chooses an appropriate accept, reject, modify, request-evidence, or escalate action.
- Explanation does not present SHAP, TCAV, LIME, or Grad-CAM output as causal proof.

A proposed initial target is at least 80% correct completion across these explanation tasks, with no Critical decision based only on an explanation graphic.

## Workflow Metrics

| Metric | Measurement |
|---|---|
| Review preparation time | Median minutes per review before and after pilot |
| Rework | Number of repeated corrections per record |
| Evidence resolution time | Hours or days from finding to accepted evidence |
| Gate resolution time | Days to resolve Critical or High blocker |
| Human modification rate | Modified model findings ÷ reviewed findings |
| Escalation rate | Escalated findings ÷ reviewed findings |

## Risk-Tier Thresholds

| Score | Tier | Governance Response |
|---:|---|---|
| 17–25 | Critical | Block or restrict launch/commissioning; executive review required |
| 10–16 | High | Mandatory mitigation, senior approval, and continuous monitoring |
| 5–9 | Medium | Standard governance gate and periodic review |
| 1–4 | Low | Authorised acceptance and routine monitoring |

## Threshold Review

Thresholds should be reviewed when:

- The domain or use case changes
- A material incident occurs
- Error rates exceed the agreed limit
- Model, dataset, supplier, or software changes materially
- Reviewer behaviour indicates over-reliance or alert fatigue
- Legal, regulatory, or contractual requirements change

## Reporting Rule

Report metric values with the number of test cases, domain breakdown, confidence interval where practical, and known dataset limitations. Do not publish a percentage without the underlying numerator and denominator.
