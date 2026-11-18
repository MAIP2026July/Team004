# Human-in-the-Loop Governance

## Governance Principle

RiskReview AI is a decision-support model. AI supports analysis and monitoring, while authorised humans remain accountable for material enterprise decisions.

## Oversight Levels

### Human-in-Command

Human product leaders and governance authorities define:

- Intended and prohibited uses
- Commercial boundaries
- Risk appetite and approval thresholds
- Data-access and supplier requirements
- Launch and commissioning criteria
- Escalation and exception authority

### Human-in-the-Loop

Domain experts review each material model finding and may:

- Accept the finding
- Reject the finding
- Modify the recommendation
- Request additional evidence
- Link or merge related risks
- Escalate the decision

### Human-on-the-Loop

Authorised personnel monitor:

- Model and data drift
- Operational incidents
- Fairness and performance indicators
- Cybersecurity and update-integrity alerts
- Supplier changes
- Residual-risk movement
- Control effectiveness

## Decision Rights

| Decision | Model Role | Human Authority |
|---|---|---|
| Detect missing or stale evidence | Identify and explain the gap | Verify evidence and decide the response |
| Suggest related risks | Propose candidates and rationale | Link, merge, or reject the suggestion |
| Detect drift or anomalies | Raise an evidence-linked alert | Investigate and approve action |
| Propose mitigation | Generate options and challenge questions | Select, modify, approve, or reject the control |
| Assign likelihood and impact | Provide evidence and analysis | Approve or revise the values |
| Accept residual risk | No autonomous authority | Designated governance authority decides |
| Approve launch or commissioning | No autonomous authority | Named human authority decides |
| Close a material risk | No autonomous authority | Risk owner and required approver decide |

## Mandatory Human Review Triggers

- Critical risk score of 17–25
- High risk score of 10–16 with unresolved controls
- Material model, dataset, software, hardware, supplier, or operating change
- Significant performance, fairness, privacy, security, or continuity concern
- Recommendation outside the approved intended use
- Missing explanation or supporting evidence
- Human override of a high-consequence recommendation

## Required Decision Record

Every material decision records:

- Risk and evidence reference
- Model, dataset, software, prompt, or rule version
- Original model finding
- Uncertainty and limitations
- Human disposition and rationale
- Reviewer and approval role
- Follow-up owner and due date
- Timestamp and governance-gate result

## Override and Escalation

An authorised override must record the reason, evidence, expected consequence, monitoring condition, and review date. Critical exceptions require approval from the designated governance decision authority.
