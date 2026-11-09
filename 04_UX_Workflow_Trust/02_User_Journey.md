# RiskReview AI: User Journey

## 1. Purpose

This document describes the initial end-to-end user journey for RiskReview AI within a Tier 1 or Tier 2 automotive component New Product Development or New Product Introduction programme.

The journey covers the monthly programme-risk and launch-readiness review from Advanced Product Quality Planning to Start of Production. It shows where deterministic rules, AI-assisted review and human judgement are used.

This is the **initial proposed journey** and will be revised after stakeholder interviews, PRD validation and prototype usability testing.

---

## 2. Primary User

**Primary user:** APQP Coordinator or NPD Project Manager

The primary user prepares the monthly programme-risk review by collecting updates from workstream risk owners, checking register quality, following up on incomplete actions and preparing the review agenda.

## 3. Supporting Users

- Risk Owner
- Programme Manager
- Design Engineering representative
- Manufacturing Engineering representative
- Quality Manager
- Supplier Quality representative
- Procurement representative
- Tooling representative
- Validation representative
- Logistics representative

## 4. User Goal

> When we prepare the monthly programme-risk and launch-readiness review, we want to identify incomplete, unclear, related, stale or weakly controlled risks before the meeting so that the cross-functional team can focus on preventive decisions, accountable ownership and customer milestones.

---

## 5. Current Journey Without RiskReview AI

1. Risk owners update entries using different writing styles and levels of detail.
2. The APQP Coordinator manually checks required fields, owners, actions and dates.
3. The coordinator reads each risk to understand whether the cause, uncertain event and impact are clear.
4. Similar risks from different workstreams are identified using personal memory.
5. Weak mitigation actions are usually challenged during the meeting.
6. Missing evidence is followed up through email, calls or separate notes.
7. The review agenda is manually prepared.
8. Meeting time may be spent correcting the register instead of deciding preventive actions.
9. Final changes and their reasons may not be consistently recorded.

### Main Friction

- Repetitive manual checking
- Inconsistent risk language
- Difficulty identifying related risks
- Weak or generic mitigation statements
- Stale supporting evidence
- Late discovery of incomplete entries
- Limited traceability of corrections and decisions

---

## 6. Proposed Journey With RiskReview AI

### Stage 1: Select Programme Context

The APQP Coordinator selects or enters:

- Programme name
- Automotive component
- Customer milestone
- Current APQP stage
- Planned Start-of-Production date
- Review period
- Standard risk-register template

**System behaviour:** The product loads the applicable mandatory fields, evidence-age rules, risk categories and review configuration.

**Trust requirement:** The interface clearly states which rules are customer-configured and which prototype values are illustrative.

---

### Stage 2: Upload or Open the Risk Register

The user uploads a CSV file or opens an existing fictional programme risk register.

**Deterministic checks:**

- File type and structure
- Mandatory columns
- Missing risk owner
- Missing action owner
- Missing due date
- Invalid date
- Overdue action
- Missing review date
- Missing evidence reference

**User experience:** The product displays accepted rows, rejected rows and issues requiring correction. The user can download or view the validation errors.

**Fallback:** If the file cannot be processed, the user can continue with the original register and the product records that automated review was unavailable.

---

### Stage 3: View the Register-Quality Dashboard

The APQP Coordinator sees a summary of:

- Total risks reviewed
- Risks with missing mandatory information
- Overdue actions
- Risks with unclear cause-event-impact structure
- Potentially related risks
- Weak mitigation statements
- Stale or missing evidence
- Findings requiring human review

**Important boundary:** Dashboard counts are review indicators, not final conclusions about programme health.

---

### Stage 4: Review an Individual Risk Finding

The user opens a finding and sees:

- Original risk statement
- Workstream and APQP stage
- Related customer milestone
- Finding type
- Reason for the finding
- Supporting rule or model explanation
- Confidence or uncertainty statement
- Suggested challenge question or draft structure

Example:

> Original risk: Tooling delay may affect launch.

> AI-assisted observation: The statement does not clearly identify the cause of the possible tooling delay or the specific launch impact.

> Challenge question: Which tool approval, supplier lead time or trial milestone is at risk, and how would the delay affect PPAP or Start of Production?

**Human actions:**

- Accept the finding
- Edit the suggested wording
- Reject the finding
- Defer it for discussion
- Return it to the risk owner
- Add a reason or comment

The system never modifies the programme risk without human confirmation.

---

### Stage 5: Compare Potentially Related Risks

When the system identifies semantically related entries, the user sees a side-by-side comparison:

- Original wording
- Risk category
- Workstream
- Cause
- Potential event
- Impact
- Related milestone
- Similarity explanation

The authorised user can:

- Merge the entries
- Link the entries
- Keep the entries separate
- Reject the suggestion
- Defer the decision

**Important boundary:** A similarity score is not proof that two risks are duplicates. Distinct workstream ownership or impact may justify keeping both risks.

---

### Stage 6: Review Mitigation Quality

The product examines whether the mitigation appears to address the stated cause, event or impact.

Example:

> Existing mitigation: Follow up with the tool supplier.

> Challenge question: Has the team confirmed the tool-design approval date, supplier manufacturing lead time, progress evidence, alternative capacity, trial date and accountable owner?

The product does not declare the mitigation technically adequate or inadequate. The risk owner and NPD Project Manager remain responsible for the final response.

---

### Stage 7: Review Evidence Freshness

The system flags evidence for review when:

- Evidence date exceeds the configured review interval
- Evidence source is missing
- The linked milestone has passed
- An action is overdue
- The risk has not been reviewed within the required period

The user can:

- Add current evidence
- Confirm that existing evidence remains valid
- Mark evidence as unavailable
- Assign a follow-up action
- Defer the item to the review meeting

---

### Stage 8: Confirm Findings and Prepare the Agenda

After findings have been reviewed, the NPD Project Manager confirms the verified meeting agenda.

The agenda may include:

- High-priority risks requiring a decision
- Overdue mitigation actions
- Risks with missing evidence
- Related risks requiring merge or linkage decisions
- Weak mitigation actions requiring challenge
- Risks affecting PPAP, validation or Start-of-Production milestones
- Assigned owners and next actions

Only human-confirmed findings appear in the verified agenda.

---

### Stage 9: Record Decisions and Audit History

For every reviewed finding, the audit record stores:

- Original risk text
- Finding type
- Rule, model or prompt version
- Supporting reason
- Human action
- Human rationale
- Final verified text
- Reviewer
- Timestamp

The audit history supports traceability, correction and later evaluation.

---

## 7. Confidence and Uncertainty Behaviour

### High Confidence

Use only for well-defined deterministic checks such as missing owners, invalid dates or overdue actions.

**Interface wording:**

> Required field is missing. Please add the risk owner before the review.

### Medium Confidence

Use for semantic findings supported by clear text evidence but requiring human judgement.

**Interface wording:**

> This risk may not clearly separate the cause, uncertain event and impact. Please review the highlighted text.

### Low Confidence

Use when the available information is insufficient or when the suggestion depends heavily on project context.

**Interface wording:**

> The available information is not sufficient for a dependable suggestion. Please review manually or request clarification from the risk owner.

The prototype thresholds are provisional. Production thresholds require a labelled evaluation set and approved decision policy.

---

## 8. Human-in-the-Loop Responsibilities

### Risk Owner

- Supplies and corrects programme-risk information
- Confirms technical meaning
- Proposes mitigation and evidence

### APQP Coordinator

- Reviews completeness and AI-assisted findings
- Requests missing information
- Prepares the verified agenda

### NPD Project Manager

- Confirms risk meaning and meeting priority
- Accepts, edits, rejects, links, merges or defers findings
- Owns escalation and programme-risk decisions

### RiskReview AI

- Checks objective completeness conditions
- Generates review suggestions
- Presents evidence and uncertainty
- Records human decisions

RiskReview AI does not approve PPAP, Start of Production, risk acceptance, closure, escalation, probability, impact or FMEA ratings.

---

## 9. Manual Fallback Journey

If AI processing is unavailable or unreliable:

1. Deterministic field checks continue where possible.
2. The original register remains accessible.
3. The APQP Coordinator performs manual semantic review.
4. No AI finding is presented as completed.
5. The meeting agenda can be prepared manually.
6. The temporary failure is recorded for investigation.

The fallback protects the programme review from depending entirely on an external model or service.

---

## 10. Prototype Screens Supporting the Journey

1. Programme and risk-register upload
2. Register-quality dashboard
3. Individual risk-quality finding
4. Related-risk comparison
5. Mitigation challenge
6. Human decision and audit record
7. Verified review agenda
8. Evaluation dashboard

---

## 11. Journey Measures

The proposed journey will be evaluated using:

- Time required to prepare the monthly review
- Percentage of findings accepted or usefully edited
- Human correction effort
- Related-risk suggestion precision
- Unsupported-suggestion rate
- Meaning-change incidents
- Percentage of findings with complete audit records
- User-reported usefulness
- Number of severe guardrail failures

All target values remain provisional until discovery and controlled evaluation are completed.

---

## 12. Open Questions for Discovery

- Which user should own the final agenda?
- Which risk-register fields are mandatory across target customers?
- What evidence-age rules are acceptable for different workstreams?
- How should linked risks differ from merged risks?
- Which findings require NPD Project Manager approval rather than APQP Coordinator action?
- What language is understandable without creating over-trust?
- How much correction effort is acceptable?
- Which existing automotive systems must the future product integrate with?

---

## 13. Evidence Status

This user journey is based on the current assignment hypothesis and uses fictional automotive programme examples. It has not yet been validated through completed stakeholder interviews or production use.

Before a controlled pilot, the team must validate the journey with target users and update the workflow, roles, terminology and acceptance criteria.
