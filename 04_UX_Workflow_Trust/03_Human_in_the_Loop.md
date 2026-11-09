# Human-in-the-Loop Design

## 1. Purpose

RiskReview AI is designed as a decision-support product for automotive programme-risk reviews. It helps the NPD Project Manager, APQP Coordinator and authorised Risk Owners identify risk-register quality issues before a monthly launch-readiness meeting.

The product does not replace human judgement. Every consequential programme-risk decision remains with an authorised person.

## 2. Human Accountability Principle

RiskReview AI may analyse, flag, compare, question and summarise. It must not independently:

- Assign or change risk probability
- Assign or change risk impact
- Approve or reject a mitigation action
- Merge or delete risk entries
- Escalate or close a programme risk
- Assign FMEA severity, occurrence or detection ratings
- Approve PPAP
- Approve Start of Production

The NPD Project Manager remains accountable for the final review agenda and programme-risk decisions. The APQP Coordinator manages review preparation and evidence completeness. Risk Owners remain responsible for the meaning, ownership and treatment of their risks.

## 3. Human Roles

### 3.1 Risk Owner

The Risk Owner:

- Creates or updates the risk entry
- Confirms the cause, uncertain event and impact
- Provides mitigation, contingency, owner, due date and supporting evidence
- Responds to missing-information requests
- Confirms whether an AI suggestion preserves the intended meaning

### 3.2 APQP Coordinator

The APQP Coordinator:

- Reviews completeness and quality findings
- Checks whether evidence is current and relevant
- Sends incomplete entries back to the Risk Owner
- Reviews potentially related risks before escalation to the Project Manager
- Prepares the draft launch-readiness agenda

### 3.3 NPD Project Manager

The NPD Project Manager:

- Reviews AI findings and supporting evidence
- Accepts, edits, rejects, links, merges or defers findings
- Records the reason for material decisions
- Confirms the final programme-risk review agenda
- Decides whether specialist or programme-governance escalation is needed

### 3.4 Technical or Functional Specialist

A specialist may be consulted when a finding depends on design, tooling, manufacturing, quality, supplier, validation or regulatory knowledge. The specialist provides domain evidence but does not automatically replace the accountable programme decision-maker.

## 4. Human Review by Finding Type

### 4.1 Missing Mandatory Information

RiskReview AI may identify missing owners, dates, milestones, evidence or status fields using deterministic rules.

**Human action:** The APQP Coordinator confirms whether the field is genuinely required for the specific programme context. The Risk Owner supplies or corrects the information.

### 4.2 Weak Cause-Event-Impact Structure

RiskReview AI may identify that a risk statement does not clearly distinguish the cause, uncertain event and business or programme impact.

**Human action:** The Risk Owner or APQP Coordinator may accept the finding, revise the wording, or reject it with a reason. The system must display the original text beside any suggested structure.

### 4.3 Potentially Related or Duplicate Risks

RiskReview AI may suggest that two risks are related based on semantic similarity, common milestones, work packages, causes or impacts.

**Human action:** The NPD Project Manager decides whether to:

- Merge the entries
- Link the entries
- Keep the entries separate
- Defer the decision

The product must not merge entries automatically because similar wording may represent different suppliers, work packages, locations or accountable owners.

### 4.4 Weak Mitigation Action

RiskReview AI may generate a challenge question when mitigation wording appears general, reactive, unowned, undated or unrelated to the stated cause.

**Human action:** The Risk Owner decides how to improve the mitigation. The Project Manager decides whether the mitigation is adequate for the programme review. RiskReview AI must not declare a mitigation technically sufficient.

### 4.5 Stale Evidence

RiskReview AI may flag evidence when the review date exceeds a configured interval, the referenced milestone has passed, or the evidence source is missing.

**Human action:** The APQP Coordinator confirms whether the evidence is stale. The Risk Owner provides updated evidence or records why the existing evidence remains valid.

## 5. Available Human Decisions

Every AI-assisted finding must support the following actions where relevant:

- **Accept:** The finding is correct and useful.
- **Edit:** The finding is partly useful but requires correction.
- **Reject:** The finding is incorrect or not relevant.
- **Link:** Two risks are related but should remain separate.
- **Merge:** Two entries represent the same underlying programme risk.
- **Defer:** A decision requires additional evidence or specialist review.
- **Escalate:** The finding requires authorised programme or technical review.

For merge, reject, defer and escalation decisions, the prototype should request a short reason.

## 6. Confidence and Uncertainty Behaviour

Prototype confidence values are illustrative until evaluated using a labelled dataset.

### High-confidence finding

The product may display the finding prominently with the supporting rule, text evidence or similarity reason. Human confirmation is still required.

### Medium-confidence finding

The product should display the finding as a suggestion, show the uncertainty, and ask the reviewer to confirm the context.

### Low-confidence finding

The product should avoid a strong recommendation. It should ask for clarification, additional evidence or manual review.

The interface must not present confidence as certainty or as an approved programme-risk rating.

## 7. Explanation Requirements

Each displayed finding should include:

- Original risk text
- Finding type
- Reason for the finding
- Relevant rule, missing field, text segment or comparison evidence
- Confidence or uncertainty label where applicable
- Suggested question or revision
- Available human actions
- Model, prompt or rule version

RiskReview AI should explain enough for a reviewer to make an informed decision without exposing unnecessary model internals.

## 8. Contestability and Correction

Users must be able to:

- Correct extracted fields
- Reject incorrect findings
- Explain why a suggestion is unsuitable
- Reverse an uncommitted action
- Request specialist review
- View the original and final verified text
- View the decision history

Rejected and edited findings may be used for later product evaluation only under an approved data-governance process. User feedback must not silently retrain or permanently change the product during the prototype.

## 9. Manual Fallback

If the AI service is unavailable, unstable or below an approved quality threshold:

1. Deterministic mandatory-field and date checks continue where possible.
2. AI-assisted semantic findings are marked unavailable.
3. The APQP Coordinator continues the existing manual review process.
4. No previous AI finding is treated as current without human verification.
5. The outage and fallback mode are recorded.

The product must not block the monthly risk-review meeting merely because the AI capability is unavailable.

## 10. Audit and Traceability

For every reviewed finding, the audit record should contain:

- Programme and risk identifier
- Original risk text
- Finding type
- Finding explanation
- Model, prompt or deterministic-rule version
- Reviewer name or role
- Human action
- Decision reason where required
- Final verified text
- Timestamp
- Escalation or specialist-review reference, if applicable

Audit history should be append-only in the prototype demonstration. Production retention and deletion periods remain subject to customer policy and discovery validation.

## 11. Escalation Conditions

A finding should be escalated when:

- The suggested change may alter the intended risk meaning
- Two reviewers disagree on merging materially important risks
- The matter affects a customer launch milestone or Start-of-Production readiness
- Evidence is contradictory or cannot be verified
- The finding relates to safety, regulatory or customer-specific obligations
- The AI output contains an unsupported programme fact
- Confidential information may have been exposed

## 12. Human-in-the-Loop Measures

The controlled evaluation should measure:

- Finding acceptance rate
- Finding edit rate
- Finding rejection rate
- Deferral and escalation rate
- Average human-review time per finding
- Reviewer agreement
- Meaning-change incidents
- Unsupported-fact incidents
- Percentage of findings with complete audit records
- User-reported usefulness and correction effort

These results must be reported as measured evidence. Prototype values must be labelled illustrative until testing is completed.

## 13. Hard-Coded and Configurable Elements

### Hard-coded in the prototype

- Synthetic automotive programme
- Example users and roles
- Demonstration risk entries
- Illustrative confidence values
- Sample evidence-age interval
- Example similarity scores
- Demonstration dashboard values

### Configurable in a future production product

- Customer risk taxonomy
- Mandatory fields
- APQP stages and customer milestones
- Evidence-age thresholds
- Similarity thresholds
- Reviewer roles and permissions
- Escalation routes
- Reason codes
- Prompt and model provider
- Notification and reporting rules
- Retention and deletion policy

## 14. Launch Blockers

The pilot must not proceed if RiskReview AI:

- Changes intended risk meaning without clear detection
- Fabricates programme facts or evidence
- Automatically makes consequential risk decisions
- Cannot preserve original text and decision history
- Cannot restrict access to authorised users
- Produces an unacceptable rate of incorrect merge suggestions
- Treats writing style or language fluency as risk severity
- Cannot support manual fallback

## 15. Evidence Status

This Human-in-the-Loop design is the proposed operating model for the prototype. User roles, review effort, escalation routes, thresholds and acceptance criteria remain provisional until validated through automotive stakeholder interviews and prototype usability testing.
