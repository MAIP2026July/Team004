# Trust and Explainability Design

## 1. Purpose

RiskReview AI supports monthly programme-risk and launch-readiness reviews for Tier 1 and Tier 2 automotive component manufacturers. Trust must come from visible evidence, clear product boundaries, human control and traceable decisions, not from presenting AI output as certain.

The product is designed to help an NPD Project Manager or APQP Coordinator inspect the quality and readiness of a programme risk register. It does not replace programme governance, DFMEA, PFMEA, Control Plan, MSA, SPC, PPAP or Start-of-Production approval.

## 2. Trust Principles

RiskReview AI will follow these principles:

1. **Show the original information:** Every finding must display the original risk statement, mitigation, owner, date and evidence used for review.
2. **Explain the reason:** The user must see why a risk was flagged, such as a missing cause, unclear impact, overdue action, stale evidence or possible semantic similarity.
3. **Separate fact from inference:** Deterministic validation results must be distinguished from AI-assisted interpretations.
4. **Communicate uncertainty:** The interface must not present a semantic suggestion as a confirmed fact.
5. **Keep consequential decisions with humans:** Authorised users decide whether to accept, edit, reject, link, merge, defer or escalate a finding.
6. **Support correction and contestability:** Users must be able to correct the AI output and record why it was unsuitable.
7. **Preserve traceability:** The system must retain the original content, finding, human action, reason, version and timestamp.
8. **Fail safely:** If the AI service is unavailable or uncertainty is too high, the product should retain deterministic checks and allow manual review.

## 3. Information Classification

The interface should label each output using one of the following categories.

### Confirmed fact

A value directly available in the risk register or verified programme context.

Examples:

- Risk owner is blank.
- Mitigation due date is overdue.
- The referenced PPAP milestone date has passed.
- Supporting evidence has not been updated within the configured review interval.

### Deterministic rule result

A conclusion produced from an explicit and configurable rule.

Examples:

- Mandatory action owner is missing.
- Review date is invalid.
- Action status is open after the due date.

### AI-assisted inference

A semantic interpretation requiring human review.

Examples:

- The statement may not clearly identify the cause.
- Two risks may describe the same underlying supplier-readiness issue.
- The mitigation may not directly address the stated cause or impact.

### Recommendation

A proposed question or next step that the user may accept, modify or reject.

Example:

> Consider confirming the tool-design approval date, supplier manufacturing lead time, trial schedule, contingency capacity and accountable action owner.

### Unknown or insufficient information

The product should state when evidence is insufficient instead of creating an unsupported answer.

Example:

> The available information is insufficient to determine whether this mitigation is current. Please provide the latest evidence or review date.

## 4. Explanation Requirements by Finding Type

### Mandatory-field finding

Display:

- Missing field
- Applicable rule
- Required user action
- Whether the rule is customer-configurable

Example:

> **Finding:** Action owner is missing.  
> **Reason:** The selected automotive programme template requires an accountable action owner for every open mitigation.  
> **Required action:** Add an authorised owner or record why the field is not applicable.

### Overdue-action finding

Display:

- Due date
- Current status
- Number of overdue days
- Applicable milestone, if available

The product must not assume that an overdue action automatically means programme failure.

### Risk-statement quality finding

Display:

- Original statement
- Detected structural issue
- Suggested cause-event-impact structure
- Uncertainty notice
- Human decision controls

Example:

> **Original:** Tooling delay may affect launch.  
> **AI-assisted observation:** The statement identifies a possible event but does not clearly state the cause or measurable programme impact.  
> **Suggested structure:** Because tool-design approval may be delayed, tool manufacturing and trial production may start late, causing PPAP and Start-of-Production milestone slippage.  
> **Human action required:** Accept, edit, reject or defer.

The suggested structure must not be written directly into the official register without human confirmation.

### Potentially related-risk finding

Display:

- Both risk statements side by side
- Risk owners and workstreams
- Shared terms or semantic reason
- Related milestones
- Similarity indicator
- Merge, link, keep separate and defer controls

The product must use wording such as **potentially related** rather than **duplicate confirmed**.

### Mitigation challenge

Display:

- Risk statement
- Existing mitigation
- Reason for challenge
- Generated question
- Evidence used
- Human response field

The product should generate a question, not declare that the mitigation is technically inadequate.

### Stale-evidence finding

Display:

- Evidence source
- Last-updated date
- Configured review interval
- Reason the evidence requires review

Where the evidence date is unavailable, the product should label the condition as **missing evidence date**, not automatically as **stale evidence**.

## 5. Confidence and Uncertainty Behaviour

The prototype may use illustrative confidence levels, but production thresholds must be validated and configurable.

### High confidence

Use only when the evidence is clear and the finding is supported by a reliable rule or a strongly validated pattern.

Product behaviour:

- Display the finding prominently.
- Show the evidence and reason.
- Require human confirmation before any official change.

### Medium confidence

Use when the finding is plausible but context may affect interpretation.

Product behaviour:

- Display the finding as a review suggestion.
- Ask for confirmation or additional context.
- Do not preselect merge, escalation or acceptance.

### Low confidence

Use when information is incomplete, conflicting or outside the validated pattern.

Product behaviour:

- Avoid making a strong recommendation.
- Request additional information or route the item to manual review.
- Record that the product abstained because confidence was insufficient.

## 6. User Control and Contestability

For every AI-assisted finding, authorised users must be able to:

- Accept the suggestion
- Edit the suggestion
- Reject the suggestion
- Link related risks
- Merge risks after human review
- Keep risks separate
- Defer the decision
- Escalate to a specialist
- Add a reason or correction

A rejected finding must not repeatedly reappear without showing the previous decision and without a defined reason for reconsideration.

## 7. Human Accountability

### Risk Owner

Responsible for providing accurate risk information, evidence and mitigation updates.

### APQP Coordinator

Responsible for reviewing completeness, structural quality, related-risk suggestions and evidence readiness before the programme meeting.

### NPD Project Manager

Responsible for final programme-level decisions, including acceptance, escalation, linking, merging, prioritisation and meeting-agenda confirmation.

### Specialist Reviewer

May be consulted for design, tooling, supplier quality, manufacturing, validation, commercial or customer-specific issues.

RiskReview AI remains an advisory product. The product must not present AI output as an authorised programme decision.

## 8. Audit and Traceability

Each reviewed finding should record:

- Programme identifier
- Risk identifier
- Original risk statement
- Finding type
- Rule, model or prompt version
- Evidence displayed
- Confidence or uncertainty level
- Suggested text or question
- Human decision
- Human rationale
- Final verified text
- Reviewer identity
- Timestamp

Audit records should be searchable and exportable for the controlled pilot. Retention periods and access rules remain configurable and require customer approval.

## 9. Safe Fallback

If the AI service is unavailable, degraded or outside the approved version, the product should:

1. Continue deterministic checks where possible.
2. Clearly state that AI-assisted semantic review is unavailable.
3. Allow manual review and agenda preparation.
4. Preserve user work without silently dropping findings.
5. Record the service condition in the audit history.
6. Prevent unsupported automated changes.

## 10. Trust Risks and Controls

### Meaning change

**Risk:** Suggested wording changes the intended programme risk.  
**Control:** Show original and suggested text side by side and require explicit human confirmation.

### False duplicate suggestion

**Risk:** Separate workstream risks are merged incorrectly.  
**Control:** Present the pair as potentially related and require human merge, link or keep-separate decisions.

### Fabricated programme fact

**Risk:** Generated content introduces an unsupported supplier, milestone, date or technical fact.  
**Control:** Ground output in approved register fields and programme context, show evidence, permit abstention and block unsupported factual additions.

### Automation bias

**Risk:** Users accept suggestions without sufficient review.  
**Control:** Require active decisions, show uncertainty, collect rationale for consequential actions and monitor rejection or override patterns.

### Writing-style bias

**Risk:** Non-native English or function-specific terminology is treated as poor risk quality.  
**Control:** Evaluate cause-event-impact logic rather than grammar, allow user correction, and test across different writing styles and automotive functions.

### Confidentiality

**Risk:** Customer, supplier or programme information is exposed.  
**Control:** Use synthetic data for the prototype, minimise input data, apply role-based access in a pilot, define retention and deletion, and use only approved processing environments.

## 11. Trust Measures

Provisional measures include:

- Percentage of findings with visible evidence
- Percentage of AI-assisted findings receiving an explicit human decision
- Acceptance, edit, rejection and defer rates
- Rate of meaning-changing suggestions
- Rate of unsupported factual suggestions
- Related-risk precision on the held-out synthetic evaluation set
- User correction effort
- Number of abstentions caused by insufficient information
- Audit-record completeness
- User-reported explanation usefulness

Targets remain provisional until the dataset, user workflow and evaluation protocol are validated.

## 12. Launch Blockers

A controlled pilot must not proceed if the prototype:

- Frequently changes intended risk meaning
- Fabricates programme facts or evidence
- Merges materially different risks without human approval
- Hides uncertainty or evidence limitations
- Prevents users from correcting or rejecting findings
- Automates probability, impact, PPAP, Start-of-Production or FMEA decisions
- Cannot preserve a complete audit trail
- Uses confidential customer or supplier data without approval
- Cannot provide a manual fallback

## 13. Hard-Coded and Configurable Elements

### Hard-coded in the demonstration prototype

- Fictional automotive programme
- Synthetic risk entries
- Example APQP stages
- Demonstration confidence values
- Example evidence-age interval
- Example user roles
- Dashboard measures
- Illustrative review findings

### Configurable in a production product

- Customer risk taxonomy
- Mandatory fields
- APQP milestones
- Evidence-age thresholds
- Similarity threshold
- Confidence thresholds
- Review and escalation roles
- Customer terminology
- Audit-retention period
- Model and prompt version
- Notifications and reports

## 14. Evidence Status

This document defines the intended trust and explainability design. The current thresholds, explanations and measures are provisional. Effectiveness must be validated through stakeholder interviews, labelled synthetic-data evaluation, usability testing and a controlled pilot before any production claim is made.
