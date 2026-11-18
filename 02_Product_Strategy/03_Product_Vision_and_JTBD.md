# Product Vision and Jobs to Be Done

## 1. Product Vision

> Enable enterprises to identify, explain, govern, and continuously monitor AI-related risks while preserving accountable human authority over material decisions.

## 2. Purpose

This document identifies the stakeholders affected by the expanded enterprise AI risk-governance framework and defines their Jobs to Be Done (JTBD). The framework serves both decision-makers and technical control owners, so it must provide different views without creating conflicting sources of truth.

## 2. Primary Stakeholders

### 2.1 Executive Risk Board

**Job to Be Done**

> When an AI-enabled product or operational system presents material enterprise exposure, I need a consolidated and evidence-based view of inherent risk, controls, residual risk, uncertainty, and accountable recommendations so that I can make a defensible acceptance, escalation, or blocking decision.

**Required information**

- Critical and high risks
- Financial and continuity consequences
- Residual-risk trend
- Unresolved control gaps
- Human recommendations
- Approval and escalation history

### 2.2 Product or Programme Leader

**Job to Be Done**

> When preparing for a product launch or major operational milestone, I need to know which AI-related risks remain open, what evidence supports the controls, and which decisions require leadership approval so that the programme can proceed without hiding material exposure.

**Required information**

- Launch-gate status
- Open mitigation actions
- Validation evidence
- Dependencies and due dates
- Residual risk
- Blockers and escalation owners

### 2.3 AI or Machine-Learning Engineer

**Job to Be Done**

> When developing or updating an AI model, I need clear risk, performance, robustness, explanation, and monitoring requirements so that the model can be tested against its intended operating conditions and governance obligations.

**Required information**

- Intended use and prohibited use
- Dataset limitations
- Performance thresholds
- Edge-case scenarios
- Explainability requirement
- Drift and retraining triggers

### 2.4 Safety and Quality Specialist

**Job to Be Done**

> When reviewing an AI-enabled function, I need traceable evidence linking hazards, failure effects, controls, tests, and residual risks so that I can challenge unsupported claims and confirm readiness for the next governance gate.

**Required information**

- Failure scenarios
- Consequence severity
- Verification and validation evidence
- Fallback behaviour
- Open deviations
- Human approval records

### 2.5 Cybersecurity Specialist

**Job to Be Done**

> When assessing an AI-enabled connected system, I need visibility into attack paths, model and data integrity, access controls, software-update protection, monitoring, and incident response so that cyber risks are controlled throughout the lifecycle.

**Required information**

- Threat scenarios
- Model provenance
- Access and signing controls
- OTA integrity evidence
- Monitoring rules
- Response and rollback plan

### 2.6 Data Governance and Privacy Specialist

**Job to Be Done**

> When data is proposed for AI training, validation, or monitoring, I need to verify purpose, rights, quality, representativeness, retention, access, and geographic restrictions so that data use is lawful, responsible, and fit for purpose.

**Required information**

- Data source and ownership
- Processing purpose
- Quality and representativeness
- Personal or sensitive data classification
- Retention and deletion rules
- Cross-border and access controls

### 2.7 Operations or Maintenance Manager

**Job to Be Done**

> When an AI system recommends an operational or maintenance action, I need a clear explanation, confidence, evidence, operating limits, and escalation route so that I can make a safe and accountable decision.

**Required information**

- Recommendation and rationale
- Confidence or uncertainty
- Supporting telemetry
- Operating boundaries
- Consequence of acting or not acting
- Override and escalation options

### 2.8 Procurement and Supplier Quality

**Job to Be Done**

> When sourcing an AI model, platform, ECU, sensor, or service, I need minimum transparency, validation, cybersecurity, update, incident, audit, and exit requirements so that the enterprise can manage supplier dependency and lifecycle risk.

**Required information**

- Model and data documentation
- Validation evidence
- Change and incident notification terms
- Audit rights
- Service and support commitments
- Portability and exit provisions

## 3. Secondary Stakeholders

| Stakeholder | Interest in the framework |
|---|---|
| Legal and Compliance | Legal obligations, contracts, liability, and regulatory traceability |
| Finance | Financial exposure, mitigation cost, and business-case assumptions |
| Internal Audit | Control design, operating effectiveness, and evidence completeness |
| Information Technology | Architecture, identity, integration, availability, and support |
| End Users | Reliable recommendations, understandable limitations, and escalation options |
| Affected Customers or Communities | Fairness, safety, privacy, communication, and redress |

## 4. Automotive-Specific Jobs to Be Done

| Stakeholder | Automotive JTBD |
|---|---|
| Vehicle Programme Manager | Understand whether AI-related ECU, supplier, and validation risks threaten Start of Production |
| ECU or ADAS Engineer | Validate model performance under thermal, timing, sensor, and edge-case constraints |
| Fleet Operations Team | Detect emerging incidents and model drift across deployed vehicles |
| OTA Release Manager | Confirm model and software-update integrity, approval, rollback, and traceability |
| Supplier Quality Engineer | Obtain transparent evidence for supplier models, datasets, changes, and incidents |

## 5. Wind-Energy-Specific Jobs to Be Done

| Stakeholder | Wind-energy JTBD |
|---|---|
| Wind-Farm Operations Manager | Decide whether an AI alert requires inspection, maintenance, or continued monitoring |
| Reliability Engineer | Validate predictive-maintenance performance and false-alert consequences |
| Control Engineer | Assess wake-steering or coordinated-control changes and operating limits |
| Field Service Team | Receive actionable evidence before dispatching offshore or remote maintenance |
| Asset Owner | Understand production, maintenance, continuity, and supplier exposure |

## 6. Human–AI Interaction Needs

Every material AI recommendation should provide:

1. The observed issue or recommendation
2. The supporting data or evidence reference
3. The relevant model version
4. Confidence, uncertainty, or limitation information
5. Expected consequence if no action is taken
6. Proposed next action
7. Responsible human reviewer
8. Accept, reject, modify, and escalate options
9. Audit record of the final decision

## 7. Priority User Needs

The initial controlled pilot should prioritise five needs:

1. A consolidated view of critical and high risks
2. Traceable evidence for each material recommendation
3. Clear human decision ownership
4. Support for override and escalation
5. Continuous monitoring of changes after deployment

## 8. Anti-Jobs and Misuse Prevention

The framework should not be used to:

- Automatically justify a predetermined launch decision
- Hide uncertainty behind a single numerical score
- Replace safety, quality, cybersecurity, or legal expertise
- Rank employees or suppliers without transparent criteria and review
- Treat explanation output as proof that a model is correct
- Close risks simply because the residual score falls below a threshold

## 9. Stakeholder Success Criteria

| Stakeholder group | Example success criterion |
|---|---|
| Executives | Material decisions show evidence, owner, rationale, and approval |
| Programme leaders | Critical blockers are visible before launch-gate meetings |
| Engineers | Model limitations and tests are traceable to risks |
| Operations | Recommendations include actionable evidence and override routes |
| Governance teams | Approvals, exceptions, and changes are auditable |
| Procurement | Supplier obligations cover documentation, changes, incidents, and exit |

## 10. Alignment with Professor Expectations

| Professor expectation | Evidence in this document |
|---|---|
| Customer and user understanding | Primary and secondary stakeholders are defined |
| Jobs to Be Done | Each primary stakeholder has a contextual JTBD statement |
| Human–AI collaboration | Information, review, override, and escalation needs are listed |
| Expanded scope | Automotive and wind-energy stakeholders are separately mapped |
| Responsible AI | Affected users, transparency, uncertainty, and redress are addressed |
| Product prioritisation | Five pilot user needs are prioritised |

## 11. Conclusion

The expanded framework is a multi-stakeholder product. Its value depends on presenting the right evidence to the right decision-maker while maintaining one traceable risk and decision record. The JTBD analysis ensures that technical AI output is converted into understandable and accountable enterprise action.
