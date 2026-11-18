# Executive Summary

## 1. Project Title

**Team004: RiskReview AI – Expanded Enterprise AI Risk Governance Framework**

---

## 2. Executive Overview

RiskReview AI is an expanded enterprise Artificial Intelligence (AI) risk-governance framework designed to support the identification, assessment, mitigation, monitoring, and escalation of AI-related risks across complex industrial environments.

The project began as a focused AI-assisted programme-risk review concept for automotive New Product Development (NPD) and New Product Introduction (NPI). It has now expanded to cover AI-enabled automotive Electronic Control Units (ECUs), Advanced Driver Assistance Systems (ADAS), connected-vehicle and Over-the-Air (OTA) update infrastructure, supplier AI governance, and wind-turbine operations.

The expanded framework connects technical AI assurance with operational, financial, data, ethical, cybersecurity, and business-continuity consequences. AI is used to detect patterns, identify model or data drift, analyse risk evidence, generate controlled test scenarios, and support continuous monitoring. Authorised humans retain decision authority over risk acceptance, launch approval, operational commissioning, escalation, and closure.

---

## 3. Enterprise Problem

Organisations increasingly depend on AI-enabled models, embedded systems, connected products, operational assets, and third-party technology providers. These systems create risks that traditional project-risk and technical-review methods may not fully capture.

Key enterprise challenges include:

- AI failure in rare, unfamiliar, or changing operating conditions
- Dataset bias and insufficient geographic or demographic representation
- Accuracy degradation after model compression or hardware optimisation
- Model, sensor, or operational-data drift after deployment
- Adversarial attacks and manipulation of connected systems
- Unauthorised modification of deployed AI models
- Compromise of OTA software and model-update infrastructure
- Limited transparency from suppliers providing black-box AI solutions
- Privacy and data-sovereignty exposure
- Vendor lock-in and concentration of critical technology supply
- Weak explanations for safety-relevant AI recommendations
- Unclear accountability when humans rely on AI-generated output

The enterprise requires a repeatable framework that links AI risk to business impact, assigns accountable owners, establishes governance thresholds, and preserves human oversight throughout the product and operational lifecycle.

---

## 4. Expanded Scope

### 4.1 Automotive AI and ECU Systems

The primary application domain includes:

- Edge-case perception failures
- ECU quantisation and thermal-latency drift
- Connected-fleet spoofing
- OTA update hijacking
- Supplier black-box AI
- Driver and vehicle data privacy
- Geographic and demographic model bias
- AI hardware and platform dependency
- Post-deployment model drift
- Fleet safety and business-continuity risks

### 4.2 Wind-Turbine Operations

The second application domain demonstrates framework transferability through:

- Predictive-maintenance model opacity
- Sensor-data quality degradation
- False maintenance recommendations
- Wake-steering model drift
- Coordinated-control risk
- Cybersecurity and continuity exposure
- AI hardware and supplier bottlenecks

### 4.3 Enterprise Governance

The cross-enterprise layer includes:

- Inherent and residual risk scoring
- A 5 × 5 likelihood-impact heatmap
- Responsible AI controls
- Explainable AI methods
- Human approval and escalation gates
- Supplier and third-party governance
- Product maturity assessment
- Phased rollout
- Continuous monitoring and auditability

---

## 5. Proposed Framework

The framework combines five components.

### 5.1 Enterprise Risk Register

A structured risk register records:

- Risk source and description
- Operational impact
- Financial impact
- Data, Responsible AI, and Explainable AI impact
- Security and business-continuity impact
- AI assessment method
- AI-supported mitigation
- Human governance control
- Inherent risk
- Residual risk
- Estimated risk reduction

### 5.2 AI-Assisted Assessment

AI-supported capabilities may include:

- Fleet and operational scenario mining
- Anomaly and incident-pattern detection
- Model and data drift detection
- Related-risk clustering
- Evidence review
- Synthetic edge-case generation
- Explanation of model output
- Early-warning recommendations

### 5.3 Human Decision Governance

The operating model uses:

- **Human-in-Command:** Humans define objectives, policies, risk appetite, prohibited uses, and decision authority.
- **Human-in-the-Loop:** Authorised experts review AI alerts, explanations, evidence, and proposed controls before material decisions.
- **Human-on-the-Loop:** Humans monitor deployed systems, drift, incidents, fairness indicators, and control effectiveness.

### 5.4 Framework Cross-Walk

The project maps risks and controls to:

- National Institute of Standards and Technology AI Risk Management Framework (NIST AI RMF) 1.0
- Responsible AI principles
- Explainable AI practices
- Porter's Five Forces
- European Union AI Act considerations
- UNECE Regulation No. 155 cybersecurity considerations
- UNECE Regulation No. 156 software-update considerations

### 5.5 Phased Implementation

A seven-stage roadmap covers:

1. Strategy and governance
2. Use-case and risk mapping
3. Data and architecture readiness
4. Model and control validation
5. Shadow-mode pilot
6. Controlled deployment
7. Continuous monitoring and scaling

---

## 6. Risk-Scoring Method

The project uses a 5 × 5 likelihood-impact model.

**Inherent Risk Score = Inherent Likelihood × Inherent Impact**

**Residual Risk Score = Residual Likelihood × Residual Impact**

**Risk Reduction Percentage = (Inherent Risk Score − Residual Risk Score) / Inherent Risk Score × 100**

The overall impact follows a worst-pillar principle across operational, financial, data and AI-governance, and enterprise security and continuity impacts.

| Score | Tier | Required governance response |
|---:|---|---|
| 17–25 | Critical | Launch or commissioning blocked; executive review required |
| 10–16 | High | Mandatory mitigation plan, senior approval, validation gates, and monitoring |
| 5–9 | Medium | Managed through standard governance gates and periodic review |
| 1–4 | Low | Accepted only by authorised personnel and monitored through routine controls |

All current scores and reduction estimates are illustrative academic assumptions unless supported by documented evidence.

---

## 7. Human–AI Decision Boundary

AI may:

- Identify unusual patterns
- Detect missing or weak evidence
- Highlight possible drift
- Propose related risks
- Generate test scenarios
- Recommend investigation priorities
- Produce explanations and monitoring alerts

AI must not independently:

- Approve a commercial launch
- Commission a high-risk operational system
- Accept a critical residual risk
- Certify regulatory or safety compliance
- Change an approved risk rating
- Close a material risk
- Replace formal engineering, quality, cybersecurity, or safety validation

This boundary ensures that AI supports decision quality without removing human accountability.

---

## 8. Expected Enterprise Value

The expected value proposition includes:

- Earlier identification of model, data, supplier, or cybersecurity issues
- Improved consistency of risk assessment and documentation
- Better traceability of controls and decisions
- Faster preparation for risk, launch, and commissioning reviews
- Stronger supplier transparency
- Improved post-deployment monitoring
- Reduced dependence on undocumented expert judgement
- A repeatable approach for scaling AI governance across use cases

These outcomes remain hypotheses until validated through a controlled pilot and documented evaluation.

---

## 9. Evaluation Approach

The project evaluation will cover three dimensions.

### 9.1 Technical Evaluation

- Detection precision and recall
- False-positive and false-negative rates
- Robustness under edge conditions
- Drift-detection sensitivity
- Explanation consistency
- System latency and availability, where relevant

### 9.2 Governance Evaluation

- Human review rate for material AI recommendations
- Acceptance, rejection, and modification rates
- Escalation response time
- Audit-log completeness
- Unresolved critical findings
- Availability of approval and rollback records

### 9.3 Business Evaluation

- Reduction in manual review effort
- Improvement in risk-record completeness
- Reduction in validation delays
- Improvement in supplier evidence availability
- Reduction in unresolved high-priority actions
- User adoption and willingness to pay

For each test case, the repository will record the input, expected result, actual result, human assessment, error category, corrective action, and conclusion.

---

## 10. Core Deliverables

The current project deliverables include:

1. Enterprise AI Risk Governance presentation
2. Enterprise AI Risk Register workbook
3. Product Features and Maturity assessment
4. Seven-Stage Rollout Roadmap
5. Five-Framework Cross-Walk
6. Risk Scoring and 5 × 5 Heatmap
7. Human–AI governance documentation
8. Responsible AI and Explainable AI documentation
9. Evaluation and error-analysis documentation
10. AI collaboration and human-verification records
11. Assumptions, limitations, and references
12. Individual contribution statement

---

## 11. Assumptions and Limitations

This is an academic enterprise AI governance and product-management project.

The current work does not:

- Certify any AI system as safe
- Demonstrate regulatory approval
- Replace engineering or cybersecurity validation
- Prove production deployment in automotive or wind-energy operations
- Validate all financial-impact estimates
- Confirm that illustrative risk reductions will occur in practice
- Treat Explainable AI output as proof of model correctness

All claims must be classified as externally sourced evidence, organisational evidence, prototype observation, expert judgement, academic assumption, synthetic example, or unvalidated hypothesis.

---

## 12. Alignment with Professor Expectations

| Professor expectation | Evidence in this project |
|---|---|
| Meaningful enterprise problem | AI-related product and operational risks across automotive and wind-energy contexts |
| Expanded and justified scope | Clear progression from one automotive workflow to enterprise AI governance |
| Appropriate use of AI | Pattern detection, drift monitoring, scenario mining, evidence analysis, and explanation |
| Product-management approach | Features, maturity, stakeholders, rollout, business value, and scaling |
| Human–AI interaction | Human-in-Command, Human-in-the-Loop, and Human-on-the-Loop model |
| Responsible AI | Fairness, privacy, accountability, transparency, reliability, and security controls |
| Explainable AI | Explanation methods, decision context, and limitations |
| Risk governance | Inherent and residual risk, heatmap, thresholds, escalation, and auditability |
| Business strategy | Supplier dependency, platform concentration, enterprise value, and commercial validation |
| Demonstrable artifacts | Governance presentation and structured risk-register workbook |
| Evaluation and evidence | Technical, governance, and business measures with test-case traceability |
| Implementation roadmap | Seven-stage progression from governance foundation to enterprise scaling |
| AI collaboration | Prompt log, AI usage log, and human-verification record |
| Critical reflection | Explicit assumptions, limitations, failure modes, and unvalidated claims |
| Team contribution | Dedicated individual contribution statement |

---

## 13. Executive Recommendation

The project should proceed through a controlled, evidence-based pilot rather than immediate enterprise deployment.

The recommended sequence is:

1. Finalise scope and terminology across all files.
2. Confirm ownership and evidence for each high and critical risk.
3. Label synthetic data, illustrative scores, and unvalidated assumptions.
4. Complete the Human–AI approval and escalation design.
5. Run the framework in shadow mode using representative scenarios.
6. Compare AI recommendations with expert decisions.
7. Document errors, overrides, and corrective actions.
8. Review residual risks before controlled deployment.
9. Scale only when technical, governance, user-value, and commercial criteria are met.

---

## 14. Conclusion

RiskReview AI has expanded from a focused automotive programme-risk review concept into an enterprise AI risk-governance framework.

The expanded project demonstrates how AI-supported detection, assessment, explanation, and monitoring can be combined with structured risk methodology, Responsible AI, Explainable AI, supplier oversight, phased implementation, and accountable human decision-making.

Automotive AI and ECU systems remain the primary domain. Wind-turbine operations demonstrate potential transferability. The project's central governance principle is that AI may support enterprise decision-making, but authorised humans retain authority over material risk acceptance, launch, commissioning, escalation, and closure.
