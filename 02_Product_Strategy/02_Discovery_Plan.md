# Discovery Plan

## 1. Purpose

The purpose of discovery is to confirm whether RiskReview AI solves a repeated and valuable problem for automotive component manufacturers before the team invests further effort in the prototype.

The discovery will focus on monthly programme-risk and launch-readiness reviews in Tier 1 and Tier 2 automotive component New Product Development and New Product Introduction programmes, from Advanced Product Quality Planning (APQP) to Start of Production.

## 2. Discovery Questions

The team will investigate the following questions:

1. How is the programme risk register currently created, updated and reviewed?
2. Who prepares the register before the monthly review meeting?
3. How much time is spent checking, correcting and consolidating risk entries?
4. Which quality problems occur most frequently?
5. How are related or duplicate risks currently identified?
6. How are weak mitigation actions challenged?
7. Which project milestones, evidence and governance records are used during the review?
8. Which decisions must remain with the Project Manager, APQP Coordinator or authorised risk owner?
9. What data is sensitive or unsuitable for an external AI service?
10. What improvement would justify a pilot or paid pilot?

## 3. Target Participants

The team will aim to interview at least five people across relevant automotive programme roles.

Preferred participants are:

- NPD Project Manager
- APQP Coordinator
- Programme Manager
- Quality Manager
- Supplier Quality Engineer or Manager
- Manufacturing Engineering Manager
- Tooling or Process Development Lead
- PMO or programme-governance reviewer

At least three participants should have direct experience with automotive component launch or programme-risk reviews.

## 4. Initial Hypotheses

The discovery will test the following assumptions:

### Hypothesis 1: Review preparation is time-consuming

Project Managers or APQP Coordinators spend significant time checking incomplete fields, inconsistent wording, overdue actions and supporting evidence before the monthly review.

### Hypothesis 2: Risk-entry quality varies across functions

Design, tooling, supplier quality, manufacturing engineering, validation and logistics teams may describe risks using different levels of detail and terminology.

### Hypothesis 3: Related risks are difficult to identify

Similar risks may be recorded separately by different workstreams, making the programme exposure harder to understand.

### Hypothesis 4: Mitigation actions are often not decision-ready

Some mitigation actions may be too general, lack an accountable owner or due date, or fail to address the stated cause.

### Hypothesis 5: Users will accept AI assistance only with human control

Users may value completeness checks, semantic review and challenge questions, but they are unlikely to accept automatic risk scoring, merging, escalation, acceptance or closure.

### Hypothesis 6: Confidentiality affects adoption

Customer programme information, drawings, supplier details, project milestones and launch risks may limit the use of public AI services.

## 5. Interview Method

Each interview should take approximately 20 to 30 minutes.

The team should:

1. Explain that the discussion concerns the current risk-review workflow, not an evaluation of the participant.
2. Ask about a recent real workflow without requesting confidential project details.
3. Record only approved notes.
4. Avoid collecting customer names, drawing numbers, supplier names or confidential programme data.
5. Ask the participant to review the proposed workflow or prototype only after documenting the current process.
6. Separate participant statements from the team’s interpretation.

## 6. Core Interview Questions

### Current workflow

1. Please describe how programme risks are created and updated before a monthly review.
2. Who checks the register before the meeting?
3. Which activities take the most time?
4. What information is commonly missing or outdated?
5. How are similar or duplicate risks handled?
6. How are weak mitigation actions challenged?

### Pain and impact

7. Approximately how much preparation time is required per review cycle?
8. What happens when the register is incomplete or unclear?
9. Which risk-quality problems create the most rework or delay?
10. Do review meetings spend time correcting the register instead of making decisions?

### Existing alternatives

11. Which tools are currently used, such as Microsoft Excel, Microsoft Project, Jira, SAP, Teamcenter or a customer-specific system?
12. Are templates, macros, validation rules or manual checklists already used?
13. What works well in the current process?
14. What should not be changed?

### AI suitability and trust

15. Which tasks could be safely assisted by deterministic rules?
16. Which tasks may benefit from AI-based semantic review?
17. Which decisions must always remain with an authorised human?
18. What information or explanation would be required before trusting an AI finding?
19. What errors would make the product unacceptable?
20. What data-protection or customer-approval conditions would apply?

### Pilot and value

21. Would a limited pilot for one programme and one risk-register format be useful?
22. Which outcome should improve first: preparation time, completeness, mitigation quality or meeting readiness?
23. What result would justify continued use or a paid pilot?
24. Who would approve a pilot and who would fund it?

## 7. Current-State Baseline

Where participants can provide non-confidential estimates, the team will capture:

- Number of risks in a typical programme register
- Number of contributors
- Frequency of risk-review meetings
- Preparation time before each review
- Meeting time spent correcting or interpreting entries
- Number of entries with missing owner, date or evidence
- Number of overdue actions
- Number of user corrections after AI or rule-based review during the pilot

All figures must be labelled as one of the following:

- Measured
- Participant estimate
- Team assumption
- Synthetic prototype value

## 8. Evidence Capture

The team will maintain a discovery evidence log containing:

- Participant role
- Interview date
- Interview method
- Workflow observations
- Repeated pain points
- Existing tools
- Trust and governance concerns
- Useful quotations, only when approved and anonymised
- Team interpretation
- Product implication
- Follow-up question

No real participant should be named in the final repository without permission.

## 9. Synthesis Method

After the interviews, the team will group findings under:

- Workflow friction
- Risk-register quality issue
- User and decision-maker need
- Existing workaround
- AI opportunity
- Deterministic-rule opportunity
- Human-control requirement
- Data or governance constraint
- Commercial or pilot signal

The team will then update:

- Customer and segment definition
- Jobs to Be Done
- Product Requirements Document
- MVP scope
- Initial PlantUML workflow
- Evaluation criteria
- MVP-to-revenue roadmap

## 10. Proceed, Rework and Stop Criteria

### Proceed to prototype validation when

- At least three target participants confirm that risk-register preparation or quality review is a repeated problem.
- At least two users identify a useful role for semantic review, related-risk suggestions or mitigation challenge questions.
- The workflow can be tested using fictional or approved non-sensitive data.
- Users accept human-supervised findings with visible evidence and correction controls.

### Rework the product concept when

- The problem exists but affects a different user, project phase or workflow.
- Deterministic rules solve most of the problem without AI.
- Users need different evidence, controls or integrations.
- The proposed MVP creates excessive review effort.

### Stop or defer when

- The problem is rare or insignificant.
- Existing tools already solve the problem adequately.
- Suitable data cannot be used safely.
- Users reject AI involvement even with human control.
- The product cannot avoid changing risk meaning or fabricating project information.

## 11. Discovery Deliverables

The discovery stage will produce:

1. Interview notes or anonymised summaries
2. Current-state workflow
3. Baseline assumptions and measured values
4. Repeated problem themes
5. Updated user and buyer definitions
6. Updated Product Requirements Document
7. Updated workflow and MVP scope
8. Evidence-based decision to proceed, rework, defer or stop

## 12. Current Evidence Status

This document defines the discovery plan. It does not claim that interviews or workflow measurements have already been completed.

Until real discovery evidence is collected, the following remain assumptions requiring validation:

- Review-preparation time
- Frequency of incomplete or duplicate risks
- User willingness to adopt AI assistance
- Buyer willingness to fund a pilot
- Acceptable accuracy and usefulness thresholds
- Data-access and deployment constraints
