# Product Requirements Document

## 1. Document Information

- **Product:** RiskReview AI
- **Team:** Team004
- **Industry:** Automotive
- **Customer Segment:** Tier 1 and Tier 2 automotive component manufacturers
- **Programme Type:** New Product Development and New Product Introduction
- **Lifecycle:** Advanced Product Quality Planning to Start of Production
- **Primary Users:** NPD Project Manager and APQP Coordinator
- **Document Status:** Initial PRD for prototype and discovery validation
- **Data Status:** Synthetic data only for the prototype

## 2. Product Overview

RiskReview AI is a human-supervised AI copilot that helps automotive programme teams prepare for monthly programme-risk and launch-readiness reviews.

The product combines deterministic checks with AI-assisted semantic review to identify incomplete risk entries, weak cause-event-impact structure, potentially related risks, stale evidence and unclear mitigation actions. The product supports human judgement but does not make final programme-risk decisions.

## 3. Problem Statement

Automotive component development programmes involve design, tooling, supplier readiness, manufacturing engineering, validation, quality planning, Production Part Approval Process and Start-of-Production milestones.

Risk entries are created by different functions and may contain:

- Missing owners, dates or evidence
- Vague or incomplete risk statements
- Similar risks recorded by different teams
- Mitigation actions that do not address the stated cause
- Outdated supporting information
- Inconsistent terminology

As a result, monthly risk-review meetings may spend time correcting and interpreting the register instead of making preventive launch-readiness decisions.

## 4. Product Goal

Enable the NPD Project Manager and APQP Coordinator to prepare a more complete, understandable and decision-ready programme risk register before the monthly review meeting.

## 5. Non-Goals

RiskReview AI will not:

- Assign programme-risk probability or impact automatically
- Replace DFMEA or PFMEA
- Assign FMEA severity, occurrence or detection ratings
- Approve Production Part Approval Process submissions
- Approve Start of Production
- Automatically accept, merge, escalate, close or delete risks
- Predict all future programme risks
- Use confidential customer or supplier data in the prototype

## 6. Target Users

### 6.1 Primary User: NPD Project Manager

The NPD Project Manager needs a decision-ready programme risk register, clear ownership, visible milestone exposure and a focused review agenda.

### 6.2 Primary User: APQP Coordinator

The APQP Coordinator needs to verify the completeness and readiness of programme risks connected with design, process development, validation, PPAP and launch milestones.

### 6.3 Supporting Users

- Risk Owners
- Design Engineering
- Tooling and Manufacturing Engineering
- Quality and Supplier Quality
- Procurement and Logistics
- Testing and Validation
- Programme Governance or PMO

## 7. Jobs to Be Done

> When we prepare the monthly programme-risk and launch-readiness review for a new automotive component programme, we want to identify unclear, incomplete, related, stale and weakly controlled risks before the meeting so that the team can focus on preventive action, accountable ownership and milestone readiness.

## 8. Initial User Workflow

```text
Risk owner creates or updates risk
→ Deterministic completeness checks
→ AI-assisted semantic review
→ APQP Coordinator reviews findings
→ Risk owner adds missing information where required
→ NPD Project Manager accepts, edits, rejects, links, merges or defers
→ Verified review agenda is generated
→ Human decision and version are recorded
```

The detailed PlantUML swimlane will be maintained in the UX, Workflow and Trust folder.

## 9. Functional Requirements

### FR-01: Programme Setup

The user must be able to create or select an automotive component programme and record:

- Programme name
- Component or product family
- Customer or customer category
- APQP phase
- Planned PPAP date
- Planned Start-of-Production date
- Programme owner

### FR-02: Risk-Register Upload

The user must be able to upload a CSV file using an approved template.

The system must:

- Validate file type and required columns
- Reject files with unsupported structure
- Display validation errors before processing
- Prevent duplicate file submission where detectable

### FR-03: Mandatory-Field Checks

The system must deterministically identify missing or invalid:

- Risk identifier
- Risk statement
- Risk owner
- Mitigation action
- Action owner
- Due date
- Review date
- Status
- Supporting evidence reference

### FR-04: Overdue-Action and Evidence-Age Checks

The system must flag:

- Actions with due dates earlier than the review date and not marked complete
- Evidence older than the configured evidence-age threshold
- Risks not reviewed within the configured review interval

The prototype threshold may be hard-coded but must be labelled as provisional.

### FR-05: Risk-Statement Quality Review

The system should assess whether the risk statement contains:

- A cause or condition
- An uncertain event
- A programme impact

The finding must explain which element appears missing or unclear. The system must not silently rewrite the register.

### FR-06: Related-Risk Suggestion

The system should identify potentially related risks using semantic similarity and shared context such as:

- Workstream
- APQP milestone
- Supplier or tool
- Cause
- Impact

The system must present the risks side by side and allow the authorised user to:

- Link
- Merge
- Keep separate
- Defer

No merge may occur without explicit human confirmation.

### FR-07: Mitigation Challenge

The system should compare the mitigation text with the stated cause, event and impact and generate a challenge question when the relationship is unclear.

The product must not declare a mitigation technically adequate or inadequate.

### FR-08: Finding Explanation

Every AI-assisted finding must display:

- Original risk text
- Finding type
- Reason for the finding
- Supporting data or rule
- Confidence or uncertainty indicator
- Suggested question or draft, where applicable

### FR-09: Human Decision Controls

An authorised user must be able to:

- Accept
- Edit
- Reject
- Link
- Merge
- Defer
- Add a reason or comment

### FR-10: Verified Review Agenda

The system must generate an agenda that can include:

- High-priority programme risks selected by authorised users
- Risks with missing information
- Overdue actions
- Related-risk decisions
- Weak mitigation findings
- Stale evidence
- Customer or launch milestones requiring discussion

The agenda must contain only human-verified findings.

### FR-11: Audit Trail

The system must record:

- Original risk text
- Finding type
- Rule, model or prompt version
- Human decision
- Decision reason
- Reviewer
- Timestamp
- Final verified text

### FR-12: Export

The user should be able to export:

- Verified findings
- Review agenda
- Audit history

The prototype may use CSV or printable HTML export.

## 10. AI and Rules Requirements

### Deterministic Rules

Deterministic rules should be used for:

- Required-field validation
- Date validation
- Overdue actions
- Missing ownership
- Evidence-age checks
- Approved status values

### AI-Assisted Capabilities

AI may be used for:

- Cause-event-impact structure review
- Semantic related-risk suggestion
- Mitigation challenge-question generation
- Controlled agenda summarisation

### Human-Controlled Decisions

Humans remain responsible for:

- Probability and impact
- Risk meaning
- Mitigation selection
- Risk linkage or merge
- Acceptance and escalation
- Closure
- PPAP and Start-of-Production decisions

## 11. Trust and Explainability Requirements

The product must:

- Separate deterministic findings from AI-assisted findings
- Display the original risk text beside suggestions
- Explain why each finding was generated
- Allow correction and rejection
- Show uncertainty when evidence is incomplete
- Avoid presenting an inference as a confirmed fact
- Preserve an audit trail
- Provide a manual fallback

## 12. Data Requirements

### Prototype Data

The prototype will use synthetic automotive programme-risk data only.

The dataset should include at least 60 entries covering:

- Design and drawing release
- Prototype availability
- Tooling
- Supplier readiness
- Material availability
- Validation
- Measurement-system readiness
- Process capability
- PFMEA action closure
- Control Plan completion
- PPAP submission
- Capacity
- Trial production
- Start of Production

### Data Governance

The prototype must not contain:

- Real customer names
- Real supplier names
- Confidential drawings
- Actual pricing or commercial terms
- Personal employee information
- Proprietary failure data

## 13. Non-Functional Requirements

### NFR-01: Usability

A first-time target user should be able to complete the main prototype workflow with minimal guidance during usability testing.

### NFR-02: Performance

The prototype should process the approved synthetic dataset within a practical demonstration time. The final production target remains to be validated.

### NFR-03: Traceability

Every displayed finding must be traceable to the original risk and the rule, prompt or model version that produced the finding.

### NFR-04: Security

The prototype must not use real confidential automotive data. A production product would require role-based access, encryption, logging and approved deployment controls.

### NFR-05: Configurability

The production design should support configurable:

- Mandatory fields
- Risk categories
- APQP milestones
- Evidence-age threshold
- Review interval
- Similarity threshold
- User roles
- Escalation path
- Reporting rules

### NFR-06: Fallback

If the AI-assisted service is unavailable, deterministic checks and manual risk review must remain available.

## 14. Provisional Acceptance Criteria

The following criteria are provisional until discovery and evaluation:

- 100% of mandatory-field findings are generated through deterministic rules
- 100% of AI findings show original text and an explanation
- 100% of consequential changes require explicit human confirmation
- 0 automatic probability, impact, PPAP or Start-of-Production decisions
- 0 use of real confidential data in the prototype
- All reviewer actions are recorded in the audit trail
- The prototype supports the complete upload-to-agenda workflow
- Related-risk suggestions meet an approved precision threshold before inclusion in a controlled pilot
- Unsupported or meaning-changing suggestions remain below an agreed launch-blocking threshold

## 15. Prototype Screens

The prototype should contain:

1. Programme and risk-register upload
2. Register-quality dashboard
3. Individual risk-quality finding
4. Related-risk comparison
5. Mitigation challenge
6. Human decision and audit view
7. Verified review agenda
8. Evaluation dashboard

## 16. Success Measures

### Product Measures

- Useful-finding rate
- Acceptance, edit, rejection and defer rates
- User correction effort
- Task-completion rate
- Preparation-time change

### Technical Measures

- Related-risk precision and recall
- Agreement with human reviewers
- Unsupported-suggestion rate
- Meaning-change incident rate
- Extraction quality

### Operational Measures

- Processing time
- Human-review workload
- Cost per register
- Availability
- Fallback usage

### Business Measures

- Improvement in register completeness
- Reduction in meeting-cleaning effort
- Better launch-readiness preparation
- Willingness to continue into a paid pilot

## 17. Risks and Launch Blockers

Launch or pilot progression must stop or be reworked if the product:

- Changes the intended meaning of risks at an unacceptable rate
- Fabricates programme facts
- Creates unsupported risks as confirmed information
- Incorrectly merges materially different risks
- Exposes confidential data
- Encourages users to treat AI as the final decision-maker
- Cannot preserve traceability
- Produces excessive human-review workload

## 18. Dependencies

- Stakeholder discovery interviews
- Approved fictional risk-register template
- Human labelling guide
- Synthetic evaluation dataset
- Browser prototype environment
- AI service or simulated AI workflow
- PlantUML workflow
- Team review and version control through GitHub

## 19. Assumptions Requiring Validation

- Monthly risk-review preparation is a repeated and meaningful pain
- Target users will review AI findings rather than ignore them
- Risk-register formats are sufficiently consistent for an initial template
- Related-risk suggestions provide useful value
- A paid pilot is commercially relevant to the selected buyer
- Human-review workload remains manageable

## 20. Definition of Done for Prototype Version 1

Prototype Version 1 is complete when:

- The synthetic automotive risk register can be loaded
- Deterministic checks are displayed
- AI-assisted findings are demonstrated or transparently simulated
- Users can take the defined review actions
- A verified agenda is generated
- Audit information is visible
- Screenshots and demo instructions are available
- Hard-coded and configurable elements are documented
- AI self-evaluation is completed
- No unsupported production-performance claim is made
