# Evaluation Plan

## Objective

Evaluate whether RiskReview AI produces useful, evidence-linked findings while preserving human control across automotive AI and ECU, wind-energy, and cross-enterprise governance scenarios.

## Evaluation Sets

### Development Set

Used to refine prompts, rules, schemas, and interfaces. Development cases must not be counted as independent final evaluation evidence.

### Validation Set

Used to select thresholds and detect obvious failure modes before final testing.

### Test Set

Held back until the evaluation design is fixed. The test set should contain balanced domains, finding types, risk tiers, and difficult negative cases.

The current 15-row synthetic register is suitable for pipeline testing, not for making reliable production-performance claims. A larger labelled set is required for final evaluation.

## Recommended Minimum Test Design

- At least 100 independently held-out risk records for an initial academic evaluation
- At least 30 automotive records
- At least 30 wind-energy records
- At least 20 cross-enterprise governance records
- Remaining records allocated to difficult negative, incomplete, or ambiguous cases
- At least two reviewers for Critical and High cases

## Evaluation Tasks

1. Schema and field validation
2. Cause-event-impact issue detection
3. Evidence-gap detection
4. Related-risk suggestion
5. Supplier-governance issue detection
6. Explainability limitation detection
7. Human approval-gap detection
8. Drift or monitoring alert review
9. Risk-tier and gate calculation
10. Explanation usefulness

## Test Procedure

1. Freeze the rules, model, prompts, and thresholds.
2. Record model, dataset, and software versions.
3. Run the held-out test set without changing the system.
4. Compare findings with adjudicated human labels.
5. Calculate overall and domain-specific metrics.
6. Analyse Critical and High errors individually.
7. Record model findings accepted, rejected, modified, or escalated by humans.
8. Compare review time with a baseline manual process.
9. Document limitations and corrective actions.

## Business and Workflow Evaluation

Measure:

- Manual preparation time before and after the pilot
- Number of repeated corrections
- Time to find missing evidence
- Time to resolve Critical or High findings
- User acceptance and modification rate
- Unresolved actions and delay days
- Cost assumptions linked to observed time or delay data

Risk reduction, loss avoidance, ROI, and payback remain scenario projections until supported by measured pilot evidence.

## Robustness Tests

- Missing fields
- Contradictory evidence
- Very long risk descriptions
- Ambiguous or vague wording
- Duplicate records with different phrasing
- Adversarial or misleading instructions inside evidence text
- Out-of-domain records
- Model or data version mismatch
- Unsupported financial claims

## Evaluation Output

The final report should include:

- Dataset description
- Human-labelling method
- Versioned system configuration
- Metrics by domain and finding type
- Confusion matrices
- Critical-error review
- Human override analysis
- Time and workflow comparison
- Limitations and unresolved risks
