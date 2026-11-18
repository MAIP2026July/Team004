# User Stories and Acceptance Criteria

## US-01: Import Risk Records

**As a** Programme or Operations Leader, **I want** to import a structured risk register **so that** existing risks can enter the governance workflow.

**Acceptance criteria**

- Given an approved file format, when a user imports the file, then valid records are created.
- Invalid or missing mandatory values are reported by row and field.
- The import does not overwrite existing approved records without confirmation and version history.

## US-02: Review Multi-Dimensional Impact

**As an** Enterprise Risk reviewer, **I want** operational, financial, data/AI, security and continuity impacts shown separately **so that** a severe impact is not hidden by averaging.

**Acceptance criteria**

- Each dimension is visible.
- The overall impact follows the documented worst-pillar rule.
- The system records the human approver of the impact values.

## US-03: Receive Evidence-Gap Alerts

**As a** Safety, Quality or Operations specialist, **I want** missing or stale evidence flagged **so that** unsupported mitigation claims can be challenged.

**Acceptance criteria**

- The alert identifies the missing or stale evidence.
- The alert states why the evidence is required.
- The reviewer can accept, reject, modify or escalate the alert.

## US-04: Review Related-Risk Suggestions

**As a** Risk Owner, **I want** potentially related risks suggested **so that** fragmented signals can be reviewed together.

**Acceptance criteria**

- The suggestion identifies candidate risk IDs.
- A similarity rationale is displayed.
- No merge occurs without human confirmation.
- Rejected suggestions remain available in the audit history.

## US-05: Understand AI Recommendations

**As an** authorised reviewer, **I want** the rationale, evidence, model version, uncertainty and limitations **so that** I can evaluate the recommendation.

**Acceptance criteria**

- All five items are visible before disposition.
- Missing explanation information prevents approval of a material recommendation.
- The interface states that an explanation is not proof of correctness.

## US-06: Make a Human Decision

**As an** authorised reviewer, **I want** to accept, reject, modify or escalate an AI recommendation **so that** accountable human control is preserved.

**Acceptance criteria**

- Each disposition records reviewer, timestamp and justification.
- Modified output is distinguishable from the original AI output.
- Unauthorised users cannot approve Critical or High decisions.

## US-07: Enforce Governance Gates

**As an** Executive Risk reviewer, **I want** unresolved Critical conditions to block progression **so that** launch or commissioning cannot proceed without resolution.

**Acceptance criteria**

- A score of 17–25 maps to Critical.
- The gate shows the unresolved reason and accountable owner.
- Any exception requires named executive approval and justification.

## US-08: Monitor Drift

**As an** AI Engineer, **I want** model or data drift alerts **so that** post-deployment changes can be investigated.

**Acceptance criteria**

- The alert identifies the metric, threshold, period and affected model.
- The reviewer records investigation outcome and action.
- Material change triggers revalidation or restricted operation.

## US-09: Govern Supplier Evidence

**As a** Procurement or Supplier Quality reviewer, **I want** an evidence checklist **so that** third-party AI dependency can be governed.

**Acceptance criteria**

- The checklist covers model documentation, data, validation, cybersecurity, updates, incidents, audit rights and exit.
- Gaps have owner and due date.
- Critical evidence gaps can block approval.

## US-10: Audit Decisions

**As an** Internal Audit reviewer, **I want** a traceable decision history **so that** governance effectiveness can be verified.

**Acceptance criteria**

- The history contains input, AI output, human disposition, justification, versions and timestamps.
- Records cannot be silently altered.
- An authorised export preserves traceability.

## US-11: Automotive Edge-Case Review

**As an** ADAS or ECU Engineer, **I want** rare scenario clusters and validation gaps highlighted **so that** additional testing can be prioritised.

**Acceptance criteria**

- The cluster links to source scenarios or telemetry.
- The system communicates data coverage limitations.
- A domain engineer approves any test or model-change recommendation.

## US-12: Wind-Turbine Maintenance Review

**As a** Wind-Farm Operations Manager, **I want** predictive-maintenance alerts with evidence and uncertainty **so that** inspection or continued monitoring can be chosen responsibly.

**Acceptance criteria**

- The alert links to sensor and maintenance evidence.
- Acting and not-acting consequences are presented.
- A human approves maintenance dispatch or operational restriction.

## Professor-Expectation Alignment

This artifact supports the professor's expected evidence of product-management discipline, expanded enterprise scope, appropriate AI use, human oversight, Responsible AI, Explainable AI, measurable evaluation, commercial relevance, and critical reflection. Any score, target, or forecast without observed pilot evidence is labelled as an assumption or proposed target.
