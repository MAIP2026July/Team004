# Responsible AI

## 1. Purpose

Responsible Artificial Intelligence (RAI) controls how the Enterprise AI Risk Governance and Assurance Framework is designed, evaluated, deployed, and monitored. The framework applies to automotive AI and Electronic Control Unit systems as the primary domain and wind-turbine operations as the secondary domain.

## 2. Responsible AI Principles

| Principle | Product Requirement | Evidence |
|---|---|---|
| Accountability | Every material model finding, risk score, exception, launch, and commissioning decision has a named human owner and approver | Decision log, approval record, audit trail |
| Transparency | Users can distinguish deterministic-rule output, model output, and human-approved decisions | Interface labels, version history, model card |
| Explainability | Material findings show rationale, evidence, uncertainty, limitations, and next action | Explanation record, SHAP/TCAV report where suitable |
| Fairness | Performance is analysed across relevant regions, operating conditions, asset types, and affected groups | Segmented evaluation and disparity review |
| Privacy | Personal and confidential data is minimised, purpose-limited, access-controlled, retained, and deleted according to policy | Data inventory, access log, retention record |
| Reliability and Safety | High-consequence use cases require validation, fallback, rollback, restricted operation, and human approval | Test evidence, gate record, rollback test |
| Security | Model, data, supplier, access, and update integrity are protected and monitored | Threat model, signing evidence, incident log |
| Contestability | Authorised users can reject, modify, request evidence, override, and escalate findings | Human disposition record |

## 3. Human–AI Boundary

RiskReview AI may:

- Validate required fields, dates, ranges, and evidence references
- Analyse risk wording and evidence
- Identify potentially related risks
- Detect anomalies or model and data drift
- Generate control challenge questions
- Present rationale, uncertainty, and limitations

RiskReview AI must not autonomously:

- Approve likelihood or impact ratings
- Accept or close material risks
- Merge risk records
- Certify safety, quality, cybersecurity, privacy, or regulatory compliance
- Approve product launch, Start of Production, or operational commissioning
- Dispatch maintenance or change operational control without authorised review

## 4. Automotive Controls

- Evaluate regional and environmental performance for ADAS and perception models.
- Test ECU timing, thermal, memory, quantisation, and hardware constraints.
- Protect OTA model and software updates with signing, approval, rollback, and audit controls.
- Require Tier 1 and Tier 2 suppliers to provide model, dataset, validation, change, incident, and cybersecurity evidence.
- Communicate operating-design-domain and model limitations to authorised users.

## 5. Wind-Energy Controls

- Verify sensor provenance, calibration, drift, and maintenance history.
- Explain predictive-maintenance alerts with evidence and uncertainty.
- Restrict wake-steering and control-model operation to validated conditions.
- Require human approval for inspection, maintenance dispatch, restriction, or commissioning decisions.
- Monitor false alerts, missed failures, downtime, and control-performance changes.

## 6. Explainability Use

SHAP, TCAV, LIME, Grad-CAM, example-based explanations, Model Cards, and Data Sheets for Datasets may be used where suitable. An explanation must not be presented as proof of correctness or causality. The reviewer must consider model type, intended use, data coverage, uncertainty, and failure consequence.

## 7. Responsible AI Evaluation

Measure:

- Material findings receiving human review
- Findings accepted, rejected, modified, or escalated
- Critical and High errors
- Performance by domain and operating condition
- Evidence completeness
- Explanation interpretation and limitation recognition
- Privacy, security, fairness, and access incidents
- Override and automation-bias patterns

## 8. Expected Benefits

Responsible AI controls are expected to improve decision traceability, evidence quality, supplier transparency, and confidence in controlled deployment. Any claim of reduced risk, cost, recall, outage, or regulatory exposure requires measured pilot and operational evidence.
