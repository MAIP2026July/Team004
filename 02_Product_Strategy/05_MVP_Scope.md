# Minimum Viable Product Scope

## 1. MVP Objective

Demonstrate that RiskReview AI can consolidate enterprise AI risks, identify evidence and monitoring gaps, support explainable risk review, and record accountable human decisions in a controlled pilot.

## 2. MVP Users

- Product or Programme Leader
- AI or Machine-Learning Engineer
- Safety or Quality Specialist
- Cybersecurity Specialist
- Operations or Maintenance Manager
- Procurement or Supplier Quality representative
- Executive Risk reviewer

## 3. MVP Inputs

- Structured enterprise risk register
- Risk owner and accountable reviewer
- Likelihood and impact entered or approved by a human
- Mitigation actions and due dates
- Evidence references
- Model, data, software, and supplier version information
- Validation or monitoring observations
- Human comments and decisions

## 4. MVP Capabilities

### Must Have

- Import or create risk records
- Validate mandatory fields and dates
- Calculate inherent and residual scores from human-approved inputs
- Apply the 5 × 5 heatmap and governance thresholds
- Identify weak or missing evidence
- Suggest potentially related risks
- Display recommendation rationale and limitations
- Allow accept, reject, modify, and escalate actions
- Maintain an audit trail
- Block progression when unresolved critical conditions exist

### Should Have

- Basic model or data drift alerts
- Supplier evidence checklist
- Role-based risk dashboard
- Exportable review report
- Residual-risk trend

### Could Have

- Synthetic edge-case scenarios
- Portfolio-level risk analytics
- Automated cross-framework suggestions
- Advanced supplier benchmarking

### Will Not Have in the MVP

- Autonomous risk acceptance
- Autonomous launch or commissioning approval
- Regulatory or safety certification
- Unrestricted automated remediation
- Production integration across multiple enterprises

## 5. MVP Workflow

1. User imports or creates a risk record.
2. Rules validate required fields, dates, and score ranges.
3. AI analyses wording, evidence, related risks, and monitoring observations.
4. The product displays the finding, rationale, uncertainty, and supporting references.
5. An authorised user accepts, rejects, modifies, or escalates the finding.
6. The system calculates the current score from approved inputs.
7. Governance thresholds determine whether progression is allowed or blocked.
8. The system records the decision, approver, time, and justification.

## 6. Pilot Domains

- **Automotive:** Selected ECU, ADAS, connected-vehicle, OTA, supplier, or fleet-monitoring scenarios.
- **Wind energy:** Selected predictive-maintenance, sensor, or operational-monitoring scenarios.

The same governance core is used, but data fields, thresholds, reviewers, and explanations are domain-specific.

## 7. MVP Success Criteria

- All critical and high-risk test cases receive documented human review.
- All AI recommendations can be traced to input evidence and model version.
- No material decision is completed without an authorised reviewer.
- False positives and false negatives are documented.
- Users can understand and act on the recommendation or escalate uncertainty.
- The pilot demonstrates measurable improvement against the baseline workflow.

Numeric targets will be fixed after baseline collection and labelled test-case preparation.

## 8. MVP Limitations

- The pilot may use synthetic or anonymised scenarios.
- Results do not constitute safety or regulatory certification.
- Domain experts must verify output.
- Financial and risk-reduction claims remain hypotheses until evaluated.
- Cross-domain generalisation cannot be assumed from one pilot.
