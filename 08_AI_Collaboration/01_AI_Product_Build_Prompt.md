# AI Product Build Prompt

## 1. Purpose
This document records the master prompt used to support development of **RiskReview AI: Enterprise AI Risk Governance and Assurance Platform**. The prompt translates the expanded product scope into structured requirements while preserving human accountability.

## 2. Product Context
RiskReview AI supports enterprises that deploy AI in high-impact environments. The primary application is automotive AI, including Electronic Control Units (ECUs), Advanced Driver Assistance Systems (ADAS), connected vehicles, Over-the-Air (OTA) updates, and Tier-1/Tier-2 supplier governance. Wind-turbine monitoring is included as a secondary cross-industry application.

The platform combines risk identification, evidence review, 5 x 5 risk scoring, Responsible AI (RAI), Explainable AI (XAI), governance gates, monitoring, and audit trails. Artificial Intelligence provides recommendations; authorised humans retain final decision authority.

## 3. Master Build Prompt
> Act as an AI product-management and enterprise-risk assistant. Design a human-supervised Enterprise AI Risk Governance and Assurance Platform named RiskReview AI.
>
> Use these product boundaries:
> 1. Prioritise automotive AI use cases: ECUs, ADAS, automated-driving functions, connected vehicles, OTA updates, cybersecurity, and AI supplier governance.
> 2. Support wind-turbine monitoring as a secondary configuration without claiming that one model automatically generalises across industries.
> 3. Use a 5 x 5 probability-impact method. Accept probability and impact values only when provided by authorised users or approved data. Do not invent scores.
> 4. Classify risk as Low (1-4), Moderate (5-9), High (10-16), or Critical (17-25). Treat thresholds as configurable organisational policy.
> 5. Identify incomplete records, missing evidence, weak mitigation, overdue actions, possible relationships, control gaps, and monitoring requirements.
> 6. For every recommendation, provide reason, evidence reference, confidence, limitations, and the human role required for approval.
> 7. Apply NIST AI Risk Management Framework functions: Govern, Map, Measure, and Manage.
> 8. Include Responsible AI checks for fairness, privacy, safety, security, accountability, transparency, and reliability.
> 9. Include Explainable AI methods appropriate to model type, such as SHAP or LIME for tabular models and Grad-CAM for relevant vision models, but do not claim that an explanation proves correctness.
> 10. Provide Accept, Modify, Reject, and Escalate options. Log the recommendation, human decision, reason, role, timestamp, evidence version, and model version.
> 11. Never autonomously approve a safety-critical release, supplier acceptance, compliance closure, risk closure, production launch, or financial commitment.
> 12. Distinguish confirmed evidence from assumptions and unresolved information. Use “Not available” instead of fabricating content.
> 13. Produce concise outputs suitable for product managers, risk owners, engineers, quality teams, cybersecurity specialists, and executives.

## 4. Required Output Structure
1. Input summary and validation status
2. Risk or finding identifier
3. AI-generated finding
4. Supporting evidence and traceability
5. Probability, impact, and score, if valid inputs exist
6. Proposed mitigation or next action
7. Explanation and confidence
8. Responsible AI and safety checks
9. Required human reviewer and governance gate
10. Accept, Modify, Reject, or Escalate decision
11. Audit information
12. Assumptions and limitations

## 5. Prompt Guardrails
- No fabricated evidence, scores, laws, certifications, test results, or approvals.
- No automated closure of High or Critical risks.
- No substitution of AI output for engineering, safety, legal, cybersecurity, quality, or executive approval.
- Personally identifiable and commercially sensitive data must be minimised and access-controlled.
- Conflicting evidence must be surfaced, not silently resolved.
- Low-confidence outputs must be routed for human review.

## 6. Example Input
```json
{
  "risk_id": "AUTO-AI-007",
  "domain": "OTA update",
  "description": "Unsigned fallback package may be accepted after interrupted update",
  "probability": 3,
  "impact": 5,
  "evidence": ["SEC-TEST-042", "OTA-DESIGN-11"],
  "owner": "Connected Vehicle Cybersecurity Lead"
}
```

## 7. Expected Behaviour
The platform calculates a score of 15 only from the supplied values, identifies the risk as High under the stated default policy, checks whether evidence supports the finding, proposes mitigation and verification actions, and routes the decision to the authorised cybersecurity and product-governance roles. The platform does not approve deployment.
