# Scaling Strategy and Constraints

## Scaling Objective

Scale RiskReview AI without reducing meaning preservation, trust, confidentiality, explainability or human accountability.

## Main Scaling Constraints

### Customer-Specific Taxonomy

Automotive customers use different risk categories, milestone names and templates. Configuration should be versioned rather than silently embedded in prompts.

### Data Confidentiality

Programme, supplier, drawing, cost and launch information may be commercially sensitive. Production deployment requires role-based access, encryption, retention rules and customer-approved hosting.

### Integration Complexity

Customers may use spreadsheets, PLM, QMS, ERP or programme-management systems. The MVP should avoid promising universal integration.

### Model and Provider Dependence

Provider changes may alter quality, cost or availability. Maintain approved versions, evaluation sets, monitoring and a manual or rules-only fallback.

### Human Review Capacity

AI findings may create additional work if precision is low. Monitor findings per register, reviewer time, acceptance, edit and rejection rates.

### Domain Transfer

Performance in one component programme does not prove suitability across all automotive categories or industries. Each expansion requires discovery and evaluation.

## Scaling Principles

- Preserve a stable product core.
- Keep customer-specific configuration separate and version controlled.
- Apply rules before model inference.
- Add programmes only after pilot thresholds are met.
- Monitor cost, latency, usefulness and severe failures by customer and version.
- Retain a safe manual workflow.

## Operational Measures

- Processing time per register
- Cost per reviewed register
- Findings per 100 entries
- Human-review minutes per finding
- Acceptance, edit and rejection rates
- Meaning-change incidents
- Unsupported-fact incidents
- Availability and fallback usage

## Scale Decision

Proceed to wider rollout only when user value, gross-margin path, confidentiality controls, monitoring and support responsibilities are demonstrated.
