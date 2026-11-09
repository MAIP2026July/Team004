# Feature Prioritisation

## 1. Purpose

This document prioritises the features of **RiskReview AI** for the initial prototype, controlled MVP, paid pilot and later product versions.

The prioritisation is based on five questions:

1. Does the feature solve the selected automotive programme-risk problem?
2. Is the feature required to demonstrate a complete monthly review workflow?
3. Can the feature be implemented and evaluated by a two-person team?
4. Can the feature operate with human supervision and synthetic data?
5. Does the feature avoid taking authority away from the NPD Project Manager, APQP Coordinator or authorised risk owner?

## 2. Prioritisation Method

The team uses the **MoSCoW method**:

- **Must Have:** Required for the MVP to deliver its core outcome.
- **Should Have:** Important, but the MVP can still function temporarily without it.
- **Could Have:** Useful after the core workflow has been validated.
- **Will Not Have Now:** Excluded because of risk, complexity, insufficient evidence or conflict with the product boundary.

The prioritisation may be revised after stakeholder interviews, PRD validation and prototype evaluation.

## 3. Must-Have Features

### 3.1 Programme and Risk-Register Input

The user must be able to select or enter:

- Fictional automotive programme name
- Component or sub-system
- Customer milestone
- APQP stage
- Risk-register review date
- Standard risk-register data

**Reason:** The product cannot review risk quality without a defined programme context and structured input.

### 3.2 Mandatory-Field Validation

The system must check for missing:

- Risk identifier
- Cause
- Uncertain event
- Impact
- Risk owner
- Mitigation action
- Action owner
- Due date
- Review date
- Status

**Implementation:** Deterministic rules, not Artificial Intelligence.

**Reason:** These are objective checks and do not require semantic inference.

### 3.3 Overdue-Action and Invalid-Date Checks

The system must identify:

- Overdue mitigation actions
- Missing due dates
- Review dates earlier than the last update
- Invalid or inconsistent date values

**Implementation:** Deterministic rules.

### 3.4 Cause-Event-Impact Quality Review

The system must assess whether a risk statement clearly describes:

- The underlying cause
- The uncertain event
- The programme impact

The system may suggest a clearer structure, but must display the original text and must not overwrite it automatically.

**Reason:** This is the principal semantic-review capability of the MVP.

### 3.5 Mitigation Challenge Questions

The system must generate questions that help the reviewer examine whether the mitigation:

- Addresses the stated cause or event
- Has an accountable owner
- Has a due date
- Includes evidence or a measurable completion condition
- Is preventive rather than only corrective
- Includes a contingency where appropriate

The system must not declare a mitigation technically adequate or inadequate.

### 3.6 Evidence-Freshness Check

The system must flag evidence for review when:

- The supporting date exceeds the configured review interval
- The evidence source is missing
- A referenced programme milestone has passed
- The risk has not been reviewed within the configured period

**Reason:** The product should identify potentially stale information without claiming that the information is definitely incorrect.

### 3.7 Human Decision Controls

For every Artificial Intelligence finding, an authorised user must be able to:

- Accept
- Edit
- Reject
- Link
- Merge
- Keep separate
- Defer
- Escalate
- Record a reason

No consequential programme-risk decision may occur without human confirmation.

### 3.8 Verified Review-Agenda Generation

The product must generate a meeting-preparation view containing only human-reviewed items, such as:

- Incomplete risks
- Overdue actions
- Weak or unclear mitigations
- Potentially related risks requiring a decision
- Stale evidence
- Risks connected with important customer or launch milestones

### 3.9 Audit Trail

The system must retain:

- Original risk text
- Finding type
- Rule, evidence or explanation
- Artificial Intelligence or rule version
- Human decision
- Human reason
- Final verified text
- Reviewer
- Timestamp

### 3.10 Synthetic-Data Labelling

All prototype data, scores, findings and results must be clearly labelled as fictional, synthetic, simulated, illustrative or provisional, as applicable.

## 4. Should-Have Features

### 4.1 Potentially Related-Risk Suggestions

The system should compare semantic meaning and identify potentially related risk entries.

The comparison screen should show:

- Both original risk statements
- Shared cause, event, impact or work package
- Similarity explanation
- Human options to merge, link or keep separate

**Condition:** This feature should remain in the paid pilot only if acceptable precision is demonstrated on a labelled synthetic evaluation set.

### 4.2 Configurable Automotive Taxonomy

The prototype should allow configuration of:

- APQP stage
- Work package
- Risk category
- Customer milestone
- Programme status

The first version may use a limited default taxonomy, but the production product should not hard-code one customer's terminology.

### 4.3 Dashboard Filters

The dashboard should allow filtering by:

- APQP stage
- Risk category
- Risk owner
- Action owner
- Due-date status
- Customer milestone
- Finding type

### 4.4 Export of Verified Agenda

The authorised user should be able to export the verified review agenda in a reusable format such as Markdown, CSV or PDF.

### 4.5 Manual Fallback

If the Artificial Intelligence component is unavailable, the product should still provide:

- Register access
- Mandatory-field checks
- Overdue-action checks
- Manual review
- Decision capture
- Audit history

## 5. Could-Have Features

### 5.1 Portfolio-Level Pattern View

A future version could identify repeated programme-risk themes across authorised projects, subject to confidentiality and access controls.

### 5.2 Approved Lessons-Learned Retrieval

The product could retrieve approved lessons from similar automotive programmes and present them as evidence for human consideration.

### 5.3 Notifications and Reminders

Future versions could send configurable reminders for:

- Overdue actions
- Evidence refresh
- Upcoming review meetings
- Deferred findings

### 5.4 Enterprise-System Integration

The product could later integrate with approved systems such as project-management, document-management or quality-management platforms.

Integration is not required to validate the first workflow.

### 5.5 Multilingual Review Support

A later version could support additional languages after language-specific evaluation and user validation.

## 6. Will Not Have in the Initial Product

The initial product will not:

- Automatically assign risk probability or impact
- Automatically calculate or alter project-risk exposure
- Replace DFMEA or PFMEA
- Assign FMEA severity, occurrence or detection ratings
- Approve PPAP
- Approve Start of Production
- Automatically create binding escalation decisions
- Automatically accept, close, merge or delete risks
- Predict all future automotive programme risks
- Estimate financial loss without validated business data
- Use confidential customer, supplier or programme data in the academic prototype
- Integrate with every automotive enterprise system

These capabilities are excluded because they introduce higher authority, validation, safety, confidentiality or integration requirements that are not justified for the first MVP.

## 7. MVP Priority Summary

### Must Have

1. Programme and risk-register input
2. Mandatory-field validation
3. Overdue-action and date checks
4. Cause-event-impact quality review
5. Mitigation challenge questions
6. Evidence-freshness checks
7. Human decision controls
8. Verified review agenda
9. Audit trail
10. Synthetic-data labelling

### Should Have

1. Potentially related-risk suggestions
2. Configurable automotive taxonomy
3. Dashboard filters
4. Verified agenda export
5. Manual fallback

### Could Have

1. Portfolio-level patterns
2. Approved lessons-learned retrieval
3. Notifications and reminders
4. Enterprise integrations
5. Multilingual support

### Will Not Have Now

1. Autonomous project-risk scoring
2. Autonomous risk decisions
3. FMEA replacement or rating
4. PPAP or Start-of-Production approval
5. Universal future-risk prediction
6. Production integration with confidential systems

## 8. Prioritisation Decision Rule

A feature should enter the MVP only if it:

- Supports the monthly programme-risk review outcome
- Can be evaluated using synthetic or approved data
- Preserves human accountability
- Has a defined acceptance criterion
- Has manageable implementation effort
- Does not require unsupported regulatory, safety or commercial claims

A feature should be deferred when it increases scope without proving the core product hypothesis.

## 9. Validation Required

The current prioritisation is provisional. Before a controlled pilot, the team must validate:

- Which findings users consider most useful
- Whether related-risk suggestions create value or additional review burden
- Which risk-register fields are mandatory in the selected organisation
- Which automotive milestones and categories must be configurable
- Whether agenda export is necessary for first use
- Which Human-in-the-Loop decisions belong to the APQP Coordinator, NPD Project Manager or risk owner
- Whether the proposed scope can support a paid pilot

## 10. Current Recommendation

Proceed with the Must-Have features for the clickable prototype. Include related-risk suggestions as a clearly labelled experimental feature. Keep all high-authority decisions outside the MVP until discovery, evaluation and governance evidence support a broader product boundary.
