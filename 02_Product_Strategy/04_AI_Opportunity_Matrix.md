# AI Opportunity Matrix

## 1. Purpose

This document evaluates which RiskReview AI capabilities should be included in the first Minimum Viable Product for automotive component New Product Development and New Product Introduction programmes.

The evaluation prevents the team from using AI where a deterministic rule is sufficient and helps prioritise capabilities according to customer value, feasibility, data readiness, risk and implementation effort.

---

## 2. Evaluation Criteria

Each opportunity is assessed using the following criteria:

- **Customer Value:** Expected usefulness for the NPD Project Manager, APQP Coordinator and risk owners
- **Business Value:** Expected contribution to review efficiency, programme governance and commercial potential
- **Technical Feasibility:** Ability to demonstrate the capability using the available prototype approach
- **Data Readiness:** Availability of suitable fictional or approved data and labels
- **Risk Level:** Potential harm caused by an incorrect output
- **MVP Priority:** Must Have, Should Have, Could Have or Not Now

Scores use a five-point scale:

- **1:** Very low
- **2:** Low
- **3:** Medium
- **4:** High
- **5:** Very high

For risk, a higher score means higher potential harm or governance concern.

---

## 3. AI Opportunity Matrix

| Opportunity | Customer Value | Business Value | Technical Feasibility | Data Readiness | Risk Level | MVP Priority |
|---|---:|---:|---:|---:|---:|---|
| Mandatory-field and overdue-action checks | 5 | 4 | 5 | 5 | 1 | Must Have |
| Cause-event-impact structure review | 5 | 5 | 4 | 4 | 3 | Must Have |
| Potentially related-risk suggestion | 4 | 4 | 4 | 3 | 4 | Should Have |
| Mitigation challenge-question generation | 5 | 4 | 4 | 4 | 3 | Must Have |
| Stale-evidence identification | 4 | 4 | 5 | 4 | 2 | Must Have |
| Verified review-agenda generation | 4 | 4 | 5 | 5 | 2 | Must Have |
| Automatic probability and impact scoring | 3 | 4 | 2 | 2 | 5 | Not Now |
| Automatic risk acceptance or closure | 2 | 3 | 2 | 1 | 5 | Not Now |
| Prediction of new future programme risks | 4 | 4 | 2 | 1 | 5 | Not Now |
| Portfolio-level risk-pattern analysis | 4 | 5 | 3 | 2 | 4 | Could Have Later |
| Integration with PLM, QMS or ERP systems | 4 | 5 | 2 | 2 | 3 | Could Have Later |

---

## 4. Opportunity Recommendations

### 4.1 Mandatory-Field and Overdue-Action Checks

**Recommended method:** Deterministic rules

The product should check whether required fields are present and whether action dates, review dates or evidence dates have passed defined limits.

Example checks include:

- Missing risk owner
- Missing action owner
- Missing due date
- Overdue mitigation action
- Missing review date
- Invalid status value
- Missing supporting evidence

This capability should not use a language model because the required logic is stable, measurable and explainable.

**MVP decision:** Include as a Must Have capability.

---

### 4.2 Cause-Event-Impact Structure Review

**Recommended method:** Natural Language Processing and structured semantic assessment

RiskReview AI should review whether a risk statement clearly explains:

1. The cause or condition
2. The uncertain event
3. The potential impact

Example weak statement:

> Tooling delay may affect launch.

Example improved structure:

> Because tool-design approval may be delayed beyond the planned release date, tool manufacturing and trial production may start late, causing PPAP and Start-of-Production milestone slippage.

The AI may suggest a revised structure, but the risk owner must confirm that the meaning has been preserved.

**Primary risk:** The AI may alter technical meaning or add unsupported facts.

**Control:** Show original and suggested text side by side and require human confirmation.

**MVP decision:** Include as a Must Have capability.

---

### 4.3 Potentially Related-Risk Suggestion

**Recommended method:** Semantic similarity and ranking

The product may identify risk entries that appear to describe the same underlying issue or have a meaningful dependency.

The system should use the wording:

> Potentially related risks

It should not automatically declare two risks to be duplicates.

The authorised reviewer may:

- Merge
- Link
- Keep separate
- Reject the suggestion
- Defer the decision

**Primary risk:** Different risks may be incorrectly merged, causing loss of ownership or technical detail.

**Control:** Human comparison and decision are mandatory. The audit record must retain both original risk entries.

**MVP decision:** Include as a Should Have capability if prototype time permits.

---

### 4.4 Mitigation Challenge-Question Generation

**Recommended method:** Grounded Generative AI

The product should examine whether the mitigation appears connected with the stated cause, event or impact and generate a review question where the relationship is unclear.

Example existing mitigation:

> Follow up with tool supplier.

Example challenge question:

> Has the team confirmed the tool-design approval date, supplier manufacturing lead time, weekly progress evidence, alternative tool-room capacity, trial schedule and accountable action owner?

RiskReview AI must not declare the mitigation technically adequate or inadequate.

**Primary risk:** The question may contain invented project facts or inappropriate automotive assumptions.

**Control:** Ground the question in approved risk-register fields and display it as a review prompt, not a decision.

**MVP decision:** Include as a Must Have capability.

---

### 4.5 Stale-Evidence Identification

**Recommended method:** Deterministic date rules supported by evidence metadata

The product should flag evidence for review when:

- The evidence date exceeds the configured review interval
- The evidence source is missing
- The related milestone has passed
- A mitigation action is overdue
- A newer approved project update conflicts with the recorded assumption

The product should not state that the evidence is wrong. It should state that the evidence may require review.

**MVP decision:** Include as a Must Have capability.

---

### 4.6 Verified Review-Agenda Generation

**Recommended method:** Controlled summarisation using only human-verified findings

The programme review agenda may include:

- High-priority risks selected by authorised users
- Overdue actions
- Risks with missing ownership
- Potentially related risks requiring a decision
- Weak mitigations requiring discussion
- Risks linked with customer or Start-of-Production milestones

Only accepted or verified findings should enter the final agenda.

**MVP decision:** Include as a Must Have capability.

---

## 5. Capabilities Excluded from the MVP

### Automatic Probability and Impact Scoring

This capability is excluded because probability and impact depend on programme context, customer commitments, technical evidence and authorised judgement.

### Automatic Risk Acceptance, Escalation or Closure

These are consequential programme-governance decisions and must remain under human control.

### Automatic FMEA Ratings

RiskReview AI will not assign Design FMEA or Process FMEA severity, occurrence or detection ratings and will not replace FMEA methods.

### PPAP or Start-of-Production Approval

RiskReview AI may surface unresolved risks related to PPAP or launch milestones, but it will not approve PPAP or Start of Production.

### Future-Risk Prediction

The prototype does not have sufficient validated historical programme data to predict new future risks reliably.

---

## 6. First-Wedge Decision

The first product wedge is:

> Monthly pre-review quality assessment of one standard programme risk register for one fictional automotive component NPD/NPI programme from APQP to Start of Production.

The first wedge combines:

- Deterministic completeness checks
- Cause-event-impact review
- Mitigation challenge questions
- Evidence-freshness checks
- Human verification
- Verified review-agenda generation

Potentially related-risk suggestions will be included if the team can create a labelled synthetic dataset and demonstrate acceptable precision.

---

## 7. AI Appropriateness Summary

RiskReview AI should use a hybrid product design:

```text
Deterministic Rules
+ Semantic AI Review
+ Grounded Question Generation
+ Human Verification
+ Audit Trail
```

The product should not use AI for every task. Rules are preferred where requirements are objective and stable. AI is used only where variable language and context need interpretation.

---

## 8. Evidence Required Before Pilot

Before recommending a controlled pilot, the team must validate:

- At least five target users confirm the workflow problem
- Users find the selected AI findings useful and understandable
- Cause-event-impact suggestions preserve intended meaning
- Potentially related-risk suggestions achieve acceptable precision
- Unsupported or fabricated project facts remain below the agreed threshold
- Human review effort remains manageable
- Confidentiality and access controls are acceptable
- The economic buyer sees enough value to consider a paid pilot

---

## 9. Current Decision

**Recommendation:** Proceed with a narrow prototype using synthetic automotive programme-risk data.

**Commercial recommendation:** Do not commit to a paid pilot or recurring price until discovery, usability evaluation and willingness-to-pay validation are completed.
