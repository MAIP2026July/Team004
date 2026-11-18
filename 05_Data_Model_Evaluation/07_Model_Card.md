# Model Card

## Model Name

**RiskReview AI – Enterprise AI Risk Governance Decision-Support Model**

## Model Purpose

Support human review of AI-related enterprise risks by validating structured records, analysing risk and evidence text, suggesting related risks, identifying governance gaps, and generating evidence-linked challenge questions.

## Intended Domains

- Automotive AI and Electronic Control Unit systems
- Advanced Driver Assistance Systems and connected vehicles
- Over-the-Air model and software updates
- Automotive supplier AI governance
- Wind-turbine predictive maintenance and operational control
- Cross-enterprise AI governance

## Intended Users

- Product and programme leaders
- AI and ECU engineers
- Safety, quality, cybersecurity, privacy, and data-governance specialists
- Operations and maintenance reviewers
- Supplier quality and procurement reviewers
- Enterprise risk and audit authorities

## Intended Uses

- Record and schema validation
- Cause-event-impact review
- Evidence-gap and freshness review
- Related-risk suggestion
- Supplier transparency review
- Explainability and governance-gap review
- Model and data drift alert support
- Human review preparation

## Out-of-Scope Uses

- Autonomous risk scoring or acceptance
- Autonomous merging or closure of risks
- Safety, quality, cybersecurity, or regulatory certification
- Autonomous launch or commissioning approval
- Employee, supplier, or customer ranking without approved criteria and human review
- Production control without a validated domain-specific safety and governance process

## Inputs

Structured risk records, evidence metadata, approved evidence content, model and data versions, monitoring observations, workflow status, and intended-use information.

## Outputs

Finding type, finding statement, rationale, evidence reference, uncertainty or confidence information, limitation, suggested next action, and model or prompt version.

## Human Oversight

Every material finding requires an authorised human disposition. Likelihood, impact, mitigation, exception, residual-risk acceptance, launch, commissioning, restriction, rollback, and closure decisions remain human responsibilities.

## Training and Evaluation Data

The current repository includes a 15-row synthetic dataset for development and pipeline testing. It does not establish production performance. Future evaluation should use a larger, independently held-out, human-labelled dataset with automotive, wind-energy, cross-enterprise, negative, ambiguous, and high-consequence cases.

## Performance Reporting

Report precision, recall, F1, false positives, false negatives, Critical/High recall, domain breakdown, finding-type breakdown, human modification, escalation, and review-time change. Report test counts and limitations with every metric.

## Limitations

- Risk language and terminology differ across organisations.
- Evidence may be incomplete, outdated, misleading, or inaccessible.
- Similarity does not prove risks have the same cause.
- Explanations do not prove correctness or causality.
- Synthetic records may not represent real operational complexity.
- Financial and risk-reduction projections depend on assumptions.
- Domain transfer requires separate data, thresholds, controls, and evaluation.

## Fairness and Responsible AI

Evaluate performance separately across relevant domains, regions, operating conditions, and affected groups where applicable. Apply data minimisation, access controls, purpose limitation, human override, auditability, and routes for challenge or escalation.

## Security Considerations

Treat evidence as untrusted input. Defend against prompt injection, malicious documents, unauthorised access, version substitution, and leakage of proprietary or personal data. Do not send confidential information to unapproved model services.

## Monitoring

Monitor model and data drift, error patterns, human overrides, alert fatigue, supplier changes, security incidents, explanation failures, and unresolved Critical or High risks. Material changes trigger reassessment and human reapproval.

## Version Record

| Field | Value |
|---|---|
| Model version | To be assigned |
| Prompt/rule version | To be assigned |
| Dataset version | Synthetic Risk Register v1.0 |
| Evaluation date | To be completed |
| Approved intended use | To be completed after controlled evaluation |
