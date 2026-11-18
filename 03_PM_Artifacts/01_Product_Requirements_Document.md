# Product Requirements Document

## 1. Product

**RiskReview AI – Expanded Enterprise AI Risk Governance Framework**

## 2. Purpose

Provide a human-supervised enterprise product for identifying, explaining, assessing, monitoring, and governing AI-related risks across automotive AI systems and wind-turbine operations.

## 3. Problem

AI risk evidence is fragmented across engineering, validation, cybersecurity, data governance, suppliers, operations, and management reviews. Enterprises need a traceable method to connect technical observations with operational, financial, ethical, cybersecurity, and continuity impacts.

## 4. Users

- Product or Programme Leader
- AI or Machine-Learning Engineer
- Safety and Quality Specialist
- Cybersecurity Specialist
- Data Governance and Privacy Specialist
- Operations or Maintenance Manager
- Procurement or Supplier Quality representative
- Executive Risk reviewer

## 5. Scope

### Primary domain

Automotive Electronic Control Units, Advanced Driver Assistance Systems, connected vehicles, Over-the-Air updates, fleet monitoring, and supplier AI.

### Secondary domain

Wind-turbine predictive maintenance, sensor monitoring, wake-steering optimisation, coordinated control, and continuity.

## 6. Functional Requirements

| ID | Requirement | Acceptance measure | Priority |
|---|---|---|---|
| FR-01 | Import or create structured risk records | Required fields are validated and errors shown | Must |
| FR-02 | Record operational, financial, data/AI, security and continuity impacts | Each risk supports all impact dimensions | Must |
| FR-03 | Calculate inherent and residual scores from human-approved likelihood and impact | Formula result matches approved 1–5 inputs | Must |
| FR-04 | Apply 5 × 5 heatmap and governance tier | Score maps to Low, Medium, High or Critical | Must |
| FR-05 | Flag missing, weak or stale evidence | Finding identifies missing item and reason | Must |
| FR-06 | Suggest potentially related risks | Suggestion includes similarity rationale; human confirms relationship | Must |
| FR-07 | Display AI rationale, evidence, model version and limitations | Reviewer can inspect all four before deciding | Must |
| FR-08 | Support accept, reject, modify and escalate actions | Every material suggestion records one human disposition | Must |
| FR-09 | Maintain audit trail | User, time, input, output, decision and justification are recorded | Must |
| FR-10 | Block unresolved Critical conditions | Progression is prevented until authorised resolution or exception | Must |
| FR-11 | Monitor model/data drift | Alert identifies metric, threshold, period and affected use case | Should |
| FR-12 | Track supplier evidence | Checklist covers model, data, validation, change, incident and exit evidence | Should |
| FR-13 | Provide role-based reporting | Users see permitted risks, actions, trends and gate status | Should |
| FR-14 | Export governance report | Export preserves evidence and decision traceability | Should |

## 7. Human-AI Requirements

- AI may identify, analyse, explain, cluster and recommend.
- Humans approve likelihood, impact, mitigation, escalation, acceptance and closure.
- Critical and High decisions require an authorised reviewer.
- Override requires justification.
- Launch and commissioning approval cannot be autonomous.

## 8. Non-Functional Requirements

| ID | Requirement | Initial criterion |
|---|---|---|
| NFR-01 | Access control | Role-based access with least privilege |
| NFR-02 | Security | Encryption in transit and at rest |
| NFR-03 | Auditability | Immutable or tamper-evident decision history |
| NFR-04 | Traceability | Version links for data, model, evidence and decision |
| NFR-05 | Explainability | Explanation appropriate to reviewer and decision |
| NFR-06 | Reliability | Safe failure, rollback or restricted-operation procedure |
| NFR-07 | Privacy | Data minimisation, purpose limitation and retention control |
| NFR-08 | Portability | Governance records exportable in an agreed format |
| NFR-09 | Accessibility | Clear labels, readable contrast and keyboard-operable review flow |

Exact latency, availability, retention and recovery targets will be fixed after architecture and pilot criticality are confirmed.

## 9. Data Requirements

- Risk identifier, source, description and owner
- Likelihood, impact and approval status
- Mitigation, due date and evidence link
- Model, dataset, software and supplier versions
- Monitoring observation and incident history
- Human decision, justification and timestamp

Synthetic or anonymised data must be labelled. Confidential data requires approved access and handling.

## 10. Responsible and Explainable AI Requirements

- Record intended and prohibited use.
- Assess representativeness and relevant bias.
- Communicate uncertainty and operating limitations.
- Provide evidence-linked explanations.
- Monitor drift and material performance changes.
- Provide override, escalation and redress routes.
- Do not treat explanation output as proof of correctness.

## 11. MVP Success Criteria

- 100% of material pilot recommendations receive a human disposition.
- 100% of Critical and High test cases show owner, evidence and approval status.
- No autonomous launch, commissioning or risk-acceptance decision occurs.
- False positives, false negatives and overrides are documented.
- Pilot users can complete the review workflow and retrieve the decision history.
- Business improvement is compared against a measured baseline.

## 12. Out of Scope

- Regulatory or safety certification
- Autonomous risk acceptance or closure
- Autonomous product launch or operational commissioning
- Replacement of formal engineering or cybersecurity validation
- Production-wide deployment without pilot evidence

## Professor-Expectation Alignment

This artifact supports the professor's expected evidence of product-management discipline, expanded enterprise scope, appropriate AI use, human oversight, Responsible AI, Explainable AI, measurable evaluation, commercial relevance, and critical reflection. Any score, target, or forecast without observed pilot evidence is labelled as an assumption or proposed target.
