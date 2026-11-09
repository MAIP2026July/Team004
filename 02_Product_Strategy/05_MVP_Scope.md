# RiskReview AI: MVP Scope

## 1. Purpose

This document defines the Minimum Viable Product (MVP) for RiskReview AI. The MVP is intentionally limited to one automotive programme-risk workflow so that Team004 can test whether the product creates useful and trustworthy value before considering wider deployment.

## 2. Selected Industry and Segment

- **Industry:** Automotive
- **Customer segment:** Tier 1 and Tier 2 automotive component manufacturers
- **Programme type:** New Product Development (NPD) and New Product Introduction (NPI)
- **Lifecycle boundary:** Advanced Product Quality Planning (APQP) to Start of Production (SOP)
- **Primary users:** NPD Project Manager and APQP Coordinator
- **Initial workflow:** Monthly programme-risk and launch-readiness review

## 3. MVP Problem Statement

Automotive NPD and NPI programmes involve multiple workstreams, including customer requirements, design, validation, tooling, supplier readiness, manufacturing engineering, quality planning, PPAP and production launch.

Risk entries are created and updated by different functional owners. The entries may contain missing information, weak cause-event-impact structure, potentially related concerns, outdated evidence or mitigation actions that are difficult to verify. As a result, the Project Manager and APQP Coordinator may spend part of the monthly review meeting correcting the register instead of making preventive launch-readiness decisions.

## 4. MVP Objective

The MVP will test whether a combination of deterministic checks, AI-assisted semantic review and human verification can improve the preparation of an automotive programme risk register before the monthly review meeting.

The MVP will not attempt to automate programme-risk ownership or launch approval.

## 5. Primary MVP Hypothesis

> If the NPD Project Manager and APQP Coordinator receive explainable, human-verifiable findings before the monthly programme-risk review, then the team can identify incomplete, unclear, potentially related, stale or weakly controlled risks earlier and prepare a more decision-ready review agenda.

## 6. MVP Users

### 6.1 Primary Users

- NPD Project Manager
- APQP Coordinator

### 6.2 Supporting Users

- Design Engineering risk owner
- Tooling risk owner
- Supplier Quality representative
- Manufacturing Engineering representative
- Validation and Testing representative
- Procurement representative
- Quality Manager
- Programme Management Office reviewer

### 6.3 Economic Buyer Hypothesis

The initial economic buyer is expected to be one of the following:

- Head of Programme Management
- Head of APQP or Quality Planning
- Project Management Office leader
- Engineering or Operations leader responsible for programme launch governance

This buyer hypothesis must be validated through discovery interviews.

## 7. MVP Input

The prototype will use one fictional automotive component programme and a standard synthetic risk register.

### Minimum input fields

- Risk ID
- Programme name
- Component or product family
- APQP phase
- Workstream or function
- Risk category
- Cause
- Uncertain event
- Impact
- Risk owner
- Mitigation action
- Action owner
- Due date
- Review date
- Supporting evidence or reference
- Last updated date
- Status
- Related customer or programme milestone

The prototype will use only fictional or synthetic data. Real customer, supplier, employee, drawing, commercial or programme data is outside the prototype scope.

## 8. MVP Capabilities

### 8.1 Deterministic completeness checks

The product will check for:

- Missing mandatory fields
- Missing risk owner
- Missing action owner
- Missing due date
- Overdue action
- Missing review date
- Invalid or inconsistent date format
- Missing evidence reference
- Evidence older than the configured review interval

### 8.2 Risk-statement quality review

The product will review whether the risk statement clearly expresses:

- A cause or condition
- An uncertain event
- A potential programme impact

The product may suggest a clearer structure, but the authorised user must verify that the intended meaning has not changed.

### 8.3 Potentially related-risk suggestions

The product will identify risk entries that appear semantically related and display the reason for the suggestion.

The user can:

- Merge
- Link
- Keep separate
- Defer the decision
- Reject the suggestion

The product will not automatically merge or delete any risk entry.

### 8.4 Mitigation challenge questions

The product will generate review questions when a mitigation appears vague, unowned, undated, unsupported or weakly connected with the stated cause or event.

Example challenge:

> Has the team confirmed the tooling approval date, supplier lead time, weekly evidence, alternative capacity and accountable action owner?

The product will not declare a mitigation technically adequate or approve the response.

### 8.5 Evidence-freshness review

The product will flag evidence for human review when:

- The last-updated date exceeds a configured interval
- The referenced milestone has passed
- A required evidence reference is missing
- The action remains open after its due date

A stale-evidence flag indicates that review is required. It does not prove that the risk or mitigation is invalid.

### 8.6 Human decision controls

For every AI-assisted finding, the authorised user can:

- Accept
- Edit
- Reject
- Link
- Merge
- Defer
- Add a decision reason

### 8.7 Verified review-agenda generation

After human review, the product will create a draft agenda containing only verified items, such as:

- Overdue actions
- Risks requiring ownership or evidence
- Potentially related risks requiring a decision
- Weak mitigation actions requiring challenge
- Risks linked to upcoming customer or SOP milestones

### 8.8 Audit record

The prototype will retain:

- Original risk text
- Finding type
- Rule, evidence or explanation
- AI or rule version
- Human decision
- Human reason
- Final verified text
- Reviewer
- Timestamp

## 9. MVP User Journey

```text
Select fictional automotive programme
→ Upload or open standard risk register
→ Validate format and mandatory fields
→ Run deterministic and AI-assisted review
→ Open each finding with evidence
→ Accept, edit, reject, link, merge or defer
→ Record a human decision reason
→ Generate verified monthly review agenda
→ View audit and evaluation summary
```

## 10. MVP Screens

The clickable prototype should include:

1. Programme and risk-register upload
2. Register-quality dashboard
3. Individual risk-quality finding
4. Potentially related-risk comparison
5. Mitigation challenge
6. Human decision and reason capture
7. Verified programme-review agenda
8. Audit and evaluation dashboard

All prototype screens must clearly label synthetic data and simulated AI output.

## 11. Explicitly Out of Scope

The MVP will not:

- Assign project-risk probability automatically
- Assign project-risk impact automatically
- Calculate or approve a final risk rating
- Replace Design FMEA or Process FMEA
- Assign FMEA severity, occurrence or detection ratings
- Approve PPAP
- Approve Start of Production
- Predict every future programme risk
- Predict warranty failure
- Approve suppliers
- Make contractual or commercial decisions
- Automatically accept, escalate, close, merge or delete risks
- Integrate with live enterprise systems
- Use confidential customer or supplier data
- Support every automotive segment, language or geography

## 12. Human-in-the-Loop Boundary

The Project Manager, APQP Coordinator or authorised risk owner remains accountable for:

- Meaning of the project risk
- Probability and impact
- Mitigation selection
- Ownership
- Escalation
- Acceptance
- Closure
- Merge or link decision
- Launch-readiness recommendation

RiskReview AI provides decision support only.

## 13. Prototype Evidence Level

The MVP prototype may contain:

- Functional deterministic checks
- Clickable workflow
- Synthetic automotive risk entries
- Simulated AI findings
- Wizard-of-Oz semantic review where required
- Illustrative thresholds and dashboard values

The repository must distinguish functional behaviour from simulated behaviour. The prototype does not prove production-level accuracy, security, scalability, fairness, economic return or regulatory compliance.

## 14. Provisional MVP Success Criteria

The following are initial validation targets, not achieved results:

- At least 80% precision for potentially related-risk suggestions on a held-out synthetic evaluation set
- At least 80% agreement with human reviewers on defined risk-structure issues
- At least 70% of displayed findings accepted or edited into a useful result during controlled evaluation
- Less than 5% unsupported or fabricated findings
- Zero autonomous probability, impact, acceptance, escalation or closure decisions
- 100% traceability for displayed findings and human decisions
- A target reduction of at least 25% in measured preparation time during a later controlled pilot

The final thresholds must be reviewed after discovery, dataset labelling and prototype testing.

## 15. MVP Stop or Rework Conditions

The MVP should be paused or reworked if:

- Findings frequently change the intended meaning of risks
- The product fabricates programme facts or evidence
- Potentially related-risk suggestions are too inaccurate for practical review
- Human verification effort exceeds the value created
- Users cannot understand why a finding was produced
- Confidentiality controls are inadequate for a controlled pilot
- The product encourages over-reliance or automatic acceptance
- Target users report that the workflow does not fit monthly risk-review preparation

## 16. MVP-to-Revenue Boundary

The MVP itself is a validation product. The first commercial offer should be a fixed-scope paid pilot for:

- One automotive component programme
- One agreed risk-register format
- A defined pilot period
- Human verification for every finding
- Limited configuration
- A documented evaluation report

Pricing remains **TBD after buyer and willingness-to-pay interviews**.

## 17. Assumptions Requiring Validation

- Monthly programme-risk preparation is a repeated and material pain point
- Target users are willing to review AI-assisted findings
- The organisation can provide approved data for a controlled pilot
- The risk-register structure is sufficiently consistent for configuration
- The economic buyer values preparation efficiency and review readiness
- Human verification can remain practical at programme scale
- A paid pilot is commercially acceptable before enterprise integration

## 18. Current Decision

**Proceed with a narrow clickable prototype and synthetic-data evaluation. Do not proceed to a real-data pilot until discovery, data governance, user validation and launch controls are complete.**
