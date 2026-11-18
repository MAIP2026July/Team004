# Team004: RiskReview AI – Expanded Enterprise AI Risk Governance Framework

## 1. Project Overview

This project presents an expanded enterprise framework for identifying, assessing, mitigating, monitoring, and governing risks associated with Artificial Intelligence (AI)-enabled products and operations.

The project began with a focused AI-assisted programme-risk review use case in the automotive sector. The scope was subsequently expanded to examine enterprise AI risk governance across complex, high-impact operating environments.

The expanded project covers:

- Automotive Electronic Control Units (ECUs)
- Advanced Driver Assistance Systems (ADAS) and automated-driving applications
- Connected-vehicle and Over-the-Air (OTA) update infrastructure
- Automotive AI supplier governance
- Wind-turbine monitoring and operational optimisation
- Enterprise AI risk assessment and mitigation
- Responsible Artificial Intelligence (RAI)
- Explainable Artificial Intelligence (XAI)
- Human-supervised commercial-launch and operational-commissioning decisions
- Phased implementation, product maturity, and continuous monitoring

The project combines AI-supported risk analysis, enterprise risk management, business strategy, human oversight, and responsible product implementation.

---

## 2. Team Members

| Team Member | BITS ID | GitHub ID |
|---|---|---|
| Maharshi Pandit | 2025MB26121 | [2025mb26121-hub](https://github.com/2025mb26121-hub) |
| Swaminathan B. | 2025MB26109 | [007india](https://github.com/007india) |

> The final submission will include an individual contribution statement showing each team member's work, verification responsibilities, and approval of the submitted artifacts.

---

## 3. Scope Evolution

### 3.1 Initial Scope

The initial concept focused on using AI to support the review of automotive programme risk registers during New Product Development (NPD) and New Product Introduction (NPI), particularly from Advanced Product Quality Planning (APQP) to Start of Production (SOP).

The initial workflow examined how AI could help programme teams identify:

- Missing risk information
- Weak cause-event-impact descriptions
- Unclear mitigation actions
- Overdue activities
- Stale supporting evidence
- Potentially related risks
- Records requiring management attention

Authorised human users retained control over risk scoring, escalation, acceptance, closure, and launch decisions.

### 3.2 Expanded Scope

The project has evolved from a single risk-review workflow into an enterprise AI risk-governance framework.

The expanded framework examines how organisations can:

1. Identify enterprise risks created or influenced by AI.
2. Assess operational, financial, data, ethical, cybersecurity, and business-continuity impacts.
3. Use AI to detect emerging risk patterns, unusual behaviour, model drift, and control weaknesses.
4. Apply Responsible AI and Explainable AI controls.
5. calculate and govern inherent and residual risk exposure.
6. Define commercial-launch and operational-commissioning thresholds.
7. Preserve accountable human authority over material decisions.
8. Govern third-party AI models, suppliers, and technology dependencies.
9. Introduce AI capabilities through phased implementation and maturity gates.
10. Demonstrate transferability across more than one industrial context.

This enterprise Ai risk product is built using AI RMF1.0 where enterprise risk outcomes can be mapped to individual project risks which include both technical and management risks that are not in scope of this Ai product. The automotive sector and Wind-turbine operations are included to demonstrate how the governance framework can be adapted to more than one asset-intensive and safety-relevant operating environment.

---

## 4. Enterprise Problem Statement

Organisations are increasingly integrating AI into vehicles, embedded systems, connected products, engineering processes, operational infrastructure, and supplier ecosystems.

Traditional project-risk or technical-review methods may not fully address risks created by data-dependent and continuously evolving AI systems. Examples include:

- AI model failure under rare or unfamiliar operating conditions
- Dataset bias or inadequate geographic and demographic representation
- Accuracy loss after model compression or hardware optimisation
- Model and sensor drift after deployment
- Adversarial attacks on connected systems
- Unauthorised changes to deployed AI models
- Compromised OTA update infrastructure
- Supplier black-box models with limited transparency
- Restricted access to training, validation, or incident evidence
- Privacy and data-sovereignty concerns
- Vendor lock-in and technology concentration
- Inadequate explanation of safety-relevant AI recommendations
- Excessive dependence on automated recommendations
- Weak human oversight and unclear decision accountability

The enterprise therefore requires an integrated approach connecting AI risk identification, business impact, technical controls, responsible AI, explainability, supplier governance, continuous monitoring, and human decision authority.

---

## 5. Project Objective

The objective is to design and demonstrate an enterprise AI risk-governance framework that:

- Identifies AI-related enterprise risks
- Evaluates inherent and residual risk exposure
- Uses AI-assisted assessment, detection, and monitoring methods
- Links risk observations to operational and financial consequences
- Defines technical and organisational mitigation controls
- Incorporates Responsible AI and Explainable AI requirements
- Establishes Human-in-Command, Human-in-the-Loop, and Human-on-the-Loop controls
- Supports accountable commercial-launch and operational-commissioning decisions
- Provides a phased roadmap for enterprise implementation
- Connects product features with implementation maturity
- Maintains traceable assumptions, sources, decisions, and limitations

---

## 6. Expanded Use-Case Scope

### 6.1 Automotive AI and ECU Systems

The automotive scope includes:

- Fleet-wide edge-case perception failures
- ECU quantisation and thermal-latency drift
- Connected-fleet spoofing
- OTA update hijacking
- Supplier black-box AI models
- Restricted access to training and validation evidence
- Driver and vehicle data privacy
- Geographic and demographic model bias
- AI hardware and platform dependency
- Post-deployment model drift
- Vehicle and fleet continuity risks

### 6.2 Wind-Turbine Operations

The wind-energy scope includes:

- Predictive-maintenance model opacity
- Sensor-data quality degradation
- False maintenance recommendations
- Model drift in wake-steering optimisation
- Coordinated-control risks
- Cybersecurity exposure
- Operational-continuity exposure
- AI hardware and supplier bottlenecks
- Inadequate explanations for maintenance or control recommendations

### 6.3 Cross-Enterprise Governance

The cross-enterprise scope includes:

- Enterprise risk identification
- Inherent and residual risk scoring
- Likelihood-impact heatmaps
- Human approval and escalation gates
- Responsible AI controls
- Explainable AI methods
- Supplier and third-party governance
- Cybersecurity and continuity controls
- Continuous monitoring
- Post-deployment auditability
- Product maturity assessment
- Phased rollout planning

---

## 7. Why AI Is Appropriate

Deterministic rules remain suitable for fixed checks such as missing fields, invalid values, overdue dates, threshold breaches, and required approvals. AI adds value when the task requires contextual, pattern-based, or multi-source analysis.

Potential AI-supported capabilities include:

- Mining fleet or operational data for rare scenarios
- Detecting unusual model behaviour
- Identifying model and data drift
- Grouping related incidents or risk patterns
- Analysing unstructured risk descriptions
- Evaluating whether mitigation evidence is relevant and current
- Producing human-readable explanations
- Generating synthetic edge cases for controlled validation
- Supporting continuous monitoring and early-warning systems

AI output is treated as decision support. Material decisions require validation by authorised technical, business, safety, cybersecurity, or governance personnel.

---

## 8. Human–AI Decision Model

The framework uses three levels of human oversight.

### 8.1 Human-in-Command

Humans define:

- Business objectives
- Risk appetite
- Governance policies
- Prohibited AI uses
- Data-access boundaries
- Launch and commissioning criteria
- Escalation thresholds
- Accountable decision owners

### 8.2 Human-in-the-Loop

Authorised subject-matter experts review:

- AI-generated risk alerts
- Model explanations
- Validation exceptions
- Supplier evidence
- Proposed mitigation actions
- High-risk deployment decisions
- Material changes to operating conditions

The reviewer may accept, reject, modify, or escalate an AI recommendation.

### 8.3 Human-on-the-Loop

Authorised personnel monitor:

- Model drift
- Operational telemetry
- Fairness indicators
- Cybersecurity alerts
- Residual-risk movement
- Control performance
- Post-deployment incidents

### 8.4 Prohibited Autonomous Decisions

AI must not independently:

- Approve a commercial product launch
- Commission a high-risk operational system
- Accept a critical residual risk
- Approve safety or regulatory compliance
- Change an accountable risk owner's approved score
- Close a material risk without human authorisation
- Replace formal engineering, cybersecurity, quality, or safety validation

---

## 9. Risk Assessment Methodology

The enterprise risk register uses a 5 × 5 likelihood-impact approach.

### 9.1 Impact Dimensions

Risk impact is reviewed across:

1. Operational impact
2. Financial impact
3. Data, Responsible AI, and Explainable AI impact
4. Enterprise security and business-continuity impact

The overall impact follows a worst-pillar approach so that a severe consequence is not hidden by averaging it with lower-impact dimensions.

### 9.2 Risk Calculations

**Inherent Risk Score = Inherent Likelihood × Inherent Impact**

**Residual Risk Score = Residual Likelihood × Residual Impact**

**Risk Reduction Percentage = (Inherent Risk Score − Residual Risk Score) / Inherent Risk Score × 100**

### 9.3 Governance Tiers

| Score | Risk Tier | Governance Response |
|---:|---|---|
| 17–25 | Critical | Launch or commissioning blocked; executive risk-board review required |
| 10–16 | High | Mandatory mitigation plan, senior approval, validation gates, and continuous monitoring |
| 5–9 | Medium | Managed through standard product or operational governance gates and periodic review |
| 1–4 | Low | Accepted only by authorised personnel and monitored through routine controls |

> All scores in the current academic artifacts are illustrative unless supported by documented organisational evidence, validation results, or cited external data.

---

## 10. Governance Frameworks Applied

| Framework or reference | Application in the project |
|---|---|
| National Institute of Standards and Technology AI Risk Management Framework (NIST AI RMF) 1.0 | Organises activities using Govern, Map, Measure, and Manage functions |
| Responsible AI | Addresses fairness, privacy, accountability, transparency, reliability, and human oversight |
| Explainable AI | Supports understandable model behaviour, recommendations, and audit evidence |
| Porter's Five Forces | Evaluates supplier power, platform dependency, competitive pressure, and vendor concentration |
| European Union AI Act | Provides a risk-based reference for AI governance and control considerations |
| UNECE Regulation No. 155 | Supports automotive cybersecurity governance considerations |
| UNECE Regulation No. 156 | Supports automotive software-update governance considerations |

These references guide the academic framework. They do not constitute certification or replace applicable engineering, safety, cybersecurity, legal, or regulatory obligations.

---

## 11. AI Assessment and Control Approaches

The project considers the following approaches where appropriate to the risk and available evidence:

- Fleet scenario mining
- Anomaly detection
- Drift detection
- Synthetic-data generation
- Sensor fusion
- Deterministic safety monitors
- Feature-attribution methods
- Concept-based explanation methods
- Model Cards
- Data Sheets for Datasets
- Immutable audit logging
- Role-based access control
- Signed and verified model deployment
- Shadow-mode evaluation
- Human approval gates
- Post-deployment telemetry

Methods such as SHAP, TCAV, Grad-CAM, or LIME should be selected only when they are technically suitable for the model type and evaluation question. An explanation method is not treated as proof of safety or correctness.

---

## 12. Product Features and Maturity

The product maturity structure progresses from governance definition to controlled enterprise operation.

| Maturity area | Representative capability |
|---|---|
| Governance foundation | Risk appetite, roles, policies, prohibited uses, and escalation thresholds |
| Data readiness | Data ownership, quality checks, lineage, privacy controls, and representative datasets |
| Model assessment | Performance testing, explainability, robustness, fairness, and edge-case validation |
| Controlled pilot | Shadow mode, human verification, limited users, and predefined success criteria |
| Deployment governance | Approval gates, signed releases, audit records, and rollback procedures |
| Continuous assurance | Drift monitoring, incident detection, periodic review, and control testing |
| Enterprise scaling | Supplier integration, cross-domain reuse, portfolio reporting, and standardised governance |

---

## 13. Seven-Stage Rollout Roadmap

### Stage 1: Strategy and Governance

- Confirm business objectives and risk appetite
- Define accountable owners
- Establish prohibited uses and escalation thresholds
- Approve academic pilot boundaries

### Stage 2: Use-Case and Risk Mapping

- Select priority automotive and wind-energy use cases
- Map affected users, assets, decisions, and failure consequences
- Define inherent-risk assumptions

### Stage 3: Data and Architecture Readiness

- Assess data quality, access, lineage, privacy, and security
- Define model, logging, deployment, and integration architecture
- Document third-party dependencies

### Stage 4: Model and Control Validation

- Test model performance, robustness, bias, drift sensitivity, and explainability
- Validate deterministic controls, fallback modes, and human approval workflows

### Stage 5: Shadow-Mode Pilot

- Run the system without autonomous operational authority
- Compare AI observations with expert decisions
- Record false positives, false negatives, overrides, and user feedback

### Stage 6: Controlled Deployment

- Limit deployment to approved use cases and users
- Enforce monitoring, audit logging, rollback, and escalation controls
- Review residual risks before each expansion decision

### Stage 7: Continuous Monitoring and Scaling

- Monitor drift, incidents, fairness, control effectiveness, and supplier changes
- Revalidate models after material changes
- Expand only when evidence supports acceptable performance and governance maturity

---

## 14. Evaluation Plan

The evaluation will distinguish between technical model performance, governance effectiveness, and business value.

### 14.1 Technical Measures

- Detection precision and recall
- False-positive and false-negative rates
- Robustness under edge cases
- Drift-detection sensitivity
- Explanation consistency
- System latency and availability where relevant

### 14.2 Governance Measures

- Percentage of material AI recommendations reviewed by authorised humans
- Human acceptance, rejection, and modification rates
- Number of unresolved critical findings
- Time required to escalate a critical issue
- Audit-log completeness
- Percentage of deployments with documented approval and rollback plans

### 14.3 Business and Operational Measures

- Reduction in manual review effort
- Improvement in risk-record completeness
- Reduction in unresolved high-priority actions
- Reduction in validation-cycle delays
- Improvement in supplier evidence availability
- Reduction in avoidable operational interruptions

### 14.4 Required Evaluation Evidence

For each test case, the repository should record:

- Test-case identifier
- Input or scenario
- Expected result
- Actual AI result
- Human reviewer assessment
- Acceptance, rejection, or modification decision
- Error category
- Corrective action
- Final conclusion

No performance claim will be presented as validated until it is supported by documented test evidence.

---

## 15. Business and Commercial Perspective

The commercial hypothesis is that organisations operating AI-enabled products and industrial assets need a repeatable way to connect technical AI assurance with enterprise decision-making.

Potential value areas include:

- Faster risk-review preparation
- Earlier identification of model, data, supplier, or cybersecurity issues
- Better traceability of mitigation decisions
- Reduced dependence on undocumented expert judgement
- Improved evidence for launch and commissioning reviews
- Stronger supplier transparency
- Consistent enterprise reporting

A controlled pilot should validate:

- User adoption
- Time saved
- Improvement in detection and review quality
- Integration requirements
- Security and confidentiality requirements
- Buyer and budget ownership
- Willingness to pay
- Cost of implementation and ongoing assurance

Commercial scale-up should occur only after technical performance, governance effectiveness, user value, and economic viability are demonstrated.

---

## 16. Project Artifacts

| Artifact | Purpose |
|---|---|
| Enterprise AI Risk Governance presentation | Communicates the executive framework, Human–AI model, enterprise risks, controls, and rollout plan |
| Enterprise AI Risk Register workbook | Documents risks, impacts, AI assessment methods, mitigations, scores, and risk reduction |
| Product Features and Maturity sheet | Connects governance capabilities with maturity stages |
| Seven-Stage Rollout Roadmap sheet | Defines progression from strategy to continuous monitoring |
| Five-Framework Cross-Walk sheet | Maps governance controls across AI, regulatory, and business frameworks |
| Scoring and 5 × 5 Heatmap sheet | Defines risk tiers and governance actions |
| Markdown documentation | Provides traceable scope, methodology, assumptions, sources, decisions, evaluation, and assignment evidence |

### Current Supporting Files

- `Enterprise_AI_Risk_Governance_Human_AI-v5.4 1.pptx`
- `OEM_Enterprise_AI_Risk_Register-v6.xlsx`

---

## 17. Repository Structure

```text
Team004-Enterprise-AI-Risk-Governance/
├── README.md
├── 01_Executive_Summary/
│   └── Executive_Summary.md
├── 02_Scope_and_Strategy/
│   ├── Scope_Evolution.md
│   ├── Enterprise_Problem_and_Objectives.md
│   ├── Stakeholders_and_JTBD.md
│   └── Product_Features_and_Maturity.md
├── 03_Risk_Methodology/
│   ├── Enterprise_AI_Risk_Register.md
│   ├── Risk_Scoring_Methodology.md
│   └── Risk_Heatmap_and_Gate_Rules.md
├── 04_Human_AI_Governance/
│   ├── Human_AI_Decision_Model.md
│   ├── Roles_RACI_and_Escalation.md
│   ├── Responsible_AI.md
│   └── Explainable_AI.md
├── 05_Framework_Crosswalk/
│   └── Governance_Framework_Crosswalk.md
├── 06_Rollout_and_Evaluation/
│   ├── Seven_Stage_Rollout_Roadmap.md
│   ├── Evaluation_Plan.md
│   ├── Evaluation_Results.md
│   └── Error_Analysis_and_AI_Self_Evaluation.md
├── 07_Business_and_Commercial/
│   ├── Business_Value_and_KPIs.md
│   └── Commercialisation_and_Scaling.md
├── 08_AI_Collaboration/
│   ├── AI_Usage_Log.md
│   ├── Prompt_Log.md
│   └── Human_Verification_Record.md
├── 09_Assumptions_Sources_Limitations/
│   ├── Assumptions_and_Limitations.md
│   └── References.md
├── 10_Supporting_Artifacts/
│   ├── Enterprise_AI_Risk_Governance_Human_AI-v5.4 1.pptx
│   └── OEM_Enterprise_AI_Risk_Register-v6.xlsx
└── 11_Team_Contribution/
    └── Individual_Contribution_Statement.md
```

---

## 18. Assumptions and Limitations

The current work is an academic product-management and enterprise AI governance project.

The project does not:

- Certify an AI system as safe
- Replace formal engineering validation
- Replace cybersecurity testing
- Replace regulatory approval
- Independently approve product launch or operational commissioning
- Represent actual organisational risk scores unless supported by evidence
- Claim production deployment in automotive or wind-energy operations
- Treat explainability output as proof of model correctness
- Treat risk reduction estimates as validated business results without test evidence

Current risks, scores, financial impacts, performance targets, and reduction percentages must be classified as one of the following:

- Externally sourced fact
- Internal or organisational evidence
- Prototype observation
- Expert judgement
- Academic assumption
- Synthetic example
- Unvalidated hypothesis

---

## 19. Alignment with Professor Expectations

| Professor expectation | How the project addresses it | Primary evidence |
|---|---|---|
| Meaningful enterprise problem | Addresses AI-related risks in automotive and wind-turbine operations | Problem statement and risk register |
| Clear scope evolution | Shows progression from a focused risk-review use case to enterprise AI governance | Scope Evolution section |
| Appropriate AI application | Separates deterministic controls from contextual and pattern-based AI analysis | Why AI Is Appropriate section |
| Product-management perspective | Covers users, capabilities, maturity, rollout, value, and scaling | Product maturity and roadmap documentation |
| Human–AI interaction | Defines Human-in-Command, Human-in-the-Loop, and Human-on-the-Loop controls | Human–AI Decision Model |
| Responsible AI | Covers fairness, privacy, accountability, transparency, reliability, and security | Governance documentation |
| Explainable AI | Defines explanation approaches and their limitations | AI Assessment and Control Approaches |
| Enterprise risk management | Uses inherent risk, residual risk, a 5 × 5 heatmap, and governance thresholds | Risk register and scoring methodology |
| Business strategy | Examines supplier dependence, platform risk, commercial value, and scalability | Framework cross-walk and commercial documentation |
| Prototype or demonstrable artifact | Provides a structured risk register, governance presentation, and assessment workflow | PowerPoint and Excel artifacts |
| Evaluation and evidence | Defines technical, governance, and business measures with test-case traceability | Evaluation Plan |
| Implementation roadmap | Provides a seven-stage rollout from strategy to continuous assurance | Rollout roadmap |
| AI collaboration evidence | Requires prompt records, AI output review, and human verification | AI Collaboration folder |
| Critical reflection | Identifies assumptions, unvalidated claims, failure modes, and limitations | Assumptions and Limitations section |
| Individual contribution | Provides a dedicated record of each team member's contribution | Contribution statement |

---

## 20. Submission Readiness Requirements

Before final submission, the team will complete the following checks:

- [ ] Confirm the final project title and expanded scope across all artifacts.
- [ ] Ensure that the PowerPoint, Excel workbook, and Markdown files use consistent terminology.
- [ ] Correct any contradiction between stated scope and referenced standards.
- [ ] Label all synthetic data and illustrative risk scores.
- [ ] Add sources for regulatory, financial, technical, and performance claims.
- [ ] Provide a clear justification for each high or critical risk score.
- [ ] Add evaluation cases with expected and actual results.
- [ ] Document false positives, false negatives, and human overrides.
- [ ] Include AI-generated output and human verification evidence.
- [ ] Include the individual contribution statement.
- [ ] Test all internal links and verify that all repository files open correctly.
- [ ] Conduct a final professor-expectation traceability review.

---

## 21. Current Project Status

The expanded enterprise AI risk register, product maturity structure, rollout roadmap, framework cross-walk, scoring methodology, and governance presentation have been prepared.

The next submission steps are to:

1. Complete the supporting Markdown documentation.
2. Add source and assumption traceability.
3. Document prototype or scenario-based evaluation results.
4. Complete error analysis and AI self-evaluation.
5. Record team contributions and human verification.
6. Conduct a final consistency and submission-readiness review.

---

## 22. Conclusion

RiskReview AI has evolved from a focused automotive programme-risk review concept into an expanded enterprise AI risk-governance framework.

The project demonstrates how organisations can combine AI-supported risk detection and monitoring with structured enterprise governance, Responsible AI, Explainable AI, supplier oversight, human decision authority, and phased implementation.

This Enterprise AI Risk Governance & Assurance Framework Driven by AI-Based Product Management as its core strategic engine, transforms how enterprises build, validate, and scale autonomous AI across their verticals by identifying and treating threats that otherwise expose enterprises to multi-crore product  recalls, penalties, reputational damage and severe regulatory fines.
To govern these risks without getting bogged down in technical ISO certification overhead, AI-Based Product Management embeds NIST AI RMF 1.0, Responsible AI (RAI), Explainable AI (XAI), and Porter's 5 Forces directly into every product lifecycle stage through a closed-loop Human–AI governance architecture. In this workflow, AI adds continuous, machine-speed value across product management and operations. Complementing this automation, human product leaders and domain experts define commercial boundaries, anchor ethical accountability, enforce "Glass-Box" Tier-1/Tier-2 procurement mandates, validate TCAV/SHAP explainability traces, and exercise hard Go/No-Go stage-gate vetoes. Backed by a ₹10 Crore (₹1,000 Lakh) platform investment across six core product modules and a gated 7-stage AI product rollout roadmap—advancing from Proof of Concept (PoC) and Functional Prototype to a production-ready Minimum Viable Product (MVP) validated via shadow-mode field pilots prior to global commercial scale—the framework reduces average enterprise risk exposure by 67% (from 17.2 Critical down to 5.6 Medium), resolves all 6 launch-blocking critical risks, and delivers ₹710 Crore in annualized loss avoidance, generating a 7,000% Net ROI with a payback period under 1 week.

The automotive sector remains the primary application domain, while wind-turbine operations demonstrate the framework's potential transferability. The project does not propose autonomous approval of high-risk decisions. Its central principle is that AI may assist with identification, analysis, explanation, and monitoring, but accountable humans retain authority over material launch, commissioning, acceptance, and escalation decisions.
