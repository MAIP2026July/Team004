# Human Review and Final Decisions

## 1. Purpose
This document defines who reviews AI output, what decisions remain human-controlled, and how final decisions are recorded. RiskReview AI is decision support, not an autonomous approval authority.

## 2. Decision Rights
| Decision | AI role | Required human authority |
|---|---|---|
| Flag missing or inconsistent data | Detect and explain | Risk owner or data steward confirms correction |
| Suggest related risks | Rank possible relationships | Domain expert accepts, modifies, or rejects |
| Propose mitigation | Generate options and evidence | Risk owner and control owner select action |
| Calculate risk score | Calculate from approved inputs | Authorised reviewer confirms inputs and classification |
| Assess supplier evidence | Summarise gaps and conflicts | Supplier quality/procurement/governance role decides acceptance |
| Interpret model behaviour | Produce explanation | Model owner and domain expert assess sufficiency |
| Close High or Critical risk | No closure authority | Designated governance gate approves closure |
| Approve safety-critical release | No approval authority | Authorised engineering, safety, quality, and release roles decide |
| Determine legal compliance | Organise evidence only | Qualified legal/compliance authority determines applicability |
| Approve investment or scale-up | Provide analysis | Executive or authorised investment committee decides |

## 3. Review Levels
- **Level 1 – Operational review:** completeness, ownership, dates, evidence, and routine corrections.
- **Level 2 – Domain review:** engineering, quality, cybersecurity, data, model, supplier, or wind-operations expertise.
- **Level 3 – Governance review:** High/Critical risk, unresolved conflict, RAI issue, material model change, or control exception.
- **Level 4 – Executive/release gate:** safety-critical release, enterprise deployment, major investment, accepted residual Critical risk, or strategic exception.

## 4. Required Human Actions
For each material AI recommendation, the reviewer must choose:
- **Accept:** recommendation is supported and may proceed within authority.
- **Modify:** reviewer changes the recommendation and records the reason.
- **Reject:** recommendation is unsuitable or unsupported; reason is mandatory.
- **Escalate:** authority, evidence, expertise, or risk tolerance is insufficient at the current level.

No response is not approval. Timeouts and overdue decisions remain open and may trigger escalation.

## 5. Final Decision Record
```text
decision_id:
risk_or_finding_id:
ai_recommendation:
evidence_references:
model_and_prompt_version:
ai_confidence:
review_level:
decision: Accept | Modify | Reject | Escalate
final_human_decision:
decision_reason:
residual_risk:
conditions_or_follow_up:
decision_owner:
approver_role:
timestamp:
policy_version:
```

## 6. Worked Example
**Finding:** The AI flags an OTA rollback-control weakness and classifies the supplied score of 15 as High.

**AI recommendation:** Require signed fallback packages, interrupted-update recovery testing, and cybersecurity review before release.

**Human review:** The Connected Vehicle Cybersecurity Lead verifies the test evidence, modifies the recommendation to include hardware-security-module validation, and escalates release approval to the product governance gate.

**Final decision:** Release remains blocked until the revised tests pass and the authorised gate approves residual risk. The AI does not convert the recommendation into approval.

## 7. Override Control
A human may override an AI recommendation within assigned authority, but the system must capture the original recommendation, override decision, reason, evidence, role, timestamp, and follow-up. Safety or policy exceptions require the designated higher-level approval and cannot be justified only by schedule or cost pressure.

## 8. Quality Checks Before Finalisation
- Required evidence is available and current.
- Conflicting evidence has been addressed.
- Probability and impact are approved inputs.
- Explanation is understandable and relevant.
- Applicable RAI, privacy, security, and safety checks are complete.
- Reviewer has appropriate role and no unresolved conflict of interest.
- Residual risk, conditions, owner, and due date are recorded.
- Decision and policy versions are preserved in the audit trail.
