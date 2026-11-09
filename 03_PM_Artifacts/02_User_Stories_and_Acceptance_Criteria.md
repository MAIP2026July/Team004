# User Stories and Acceptance Criteria

## Product

**RiskReview AI**

## Industry and Initial Segment

- **Industry:** Automotive
- **Customer Segment:** Tier 1 and Tier 2 automotive component manufacturers
- **Programme Type:** New Product Development and New Product Introduction
- **Lifecycle:** Advanced Product Quality Planning (APQP) to Start of Production
- **Primary Users:** NPD Project Manager and APQP Coordinator
- **Initial Workflow:** Monthly programme-risk and launch-readiness review

## Purpose

This artifact converts the Product Requirements Document into testable user stories and acceptance criteria for the RiskReview AI MVP.

The acceptance criteria are provisional until validated through stakeholder interviews, workflow observation and prototype usability testing.

---

## Epic 1: Create and Validate a Programme Risk Register

### US-01: Upload a Risk Register

**As an APQP Coordinator, I want to upload a programme risk register so that I can begin the pre-review quality assessment.**

#### Acceptance Criteria

- The prototype accepts one approved CSV template.
- The prototype displays the programme name, component name, APQP stage and review date.
- The file must contain a unique risk identifier for every row.
- If the file format or mandatory columns are invalid, the system must stop processing and display the missing or incorrect columns.
- The system must not silently remove or alter uploaded rows.
- Prototype data must be fictional or synthetic.

### US-02: Validate Mandatory Fields

**As an APQP Coordinator, I want the system to identify missing mandatory fields so that incomplete risks can be corrected before the review meeting.**

#### Acceptance Criteria

- The system checks the configured mandatory fields.
- The MVP checks at least: risk ID, workstream, cause, uncertain event, impact, risk owner, mitigation, action owner, due date, review date and status.
- Each finding identifies the affected risk ID and missing field.
- The system distinguishes missing information from low-quality information.
- The user can open the affected risk directly from the finding.
- Mandatory fields must be configurable in a production version.

### US-03: Identify Overdue Actions and Invalid Dates

**As a Project Manager, I want overdue actions and invalid dates to be highlighted so that schedule-related risks receive attention before the governance meeting.**

#### Acceptance Criteria

- The system compares the action due date with the selected review date.
- An action is marked overdue only when the due date has passed and the action is not closed.
- Invalid or unreadable dates are reported separately from overdue actions.
- The system does not automatically change the action status.
- The user can filter the dashboard by overdue, due soon and invalid date.

---

## Epic 2: Review Risk-Statement Quality

### US-04: Review Cause-Event-Impact Structure

**As an NPD Project Manager, I want RiskReview AI to review whether each risk clearly states the cause, uncertain event and impact so that the register supports meaningful discussion.**

#### Acceptance Criteria

- The system evaluates the cause, uncertain event and impact fields separately.
- The finding identifies which element appears missing, vague or mixed with another element.
- The system displays the original risk statement before showing any suggestion.
- The system provides a plain-language reason for the finding.
- The system may draft a clearer structure, but the user must approve or edit it.
- The system must not overwrite the original text automatically.
- If the system lacks sufficient information, the output must state that further information is required.

### US-05: Preserve the Intended Meaning

**As a Risk Owner, I want to compare the original and suggested wording so that AI assistance does not change the intended project meaning.**

#### Acceptance Criteria

- Original and suggested wording are displayed side by side.
- Changed phrases are visually identifiable in the functional prototype or explained in text.
- The user can accept, edit, reject or defer the suggestion.
- An accepted suggestion is stored as a human-verified version.
- A rejected suggestion does not change the risk register.
- Any confirmed meaning-change incident is recorded as a severe quality failure.

---

## Epic 3: Identify Potentially Related Risks

### US-06: Suggest Related Risk Entries

**As an APQP Coordinator, I want the system to identify potentially related risks so that duplicated concerns can be compared before the review meeting.**

#### Acceptance Criteria

- The system compares risk meaning rather than relying only on identical keywords.
- Each suggestion displays both original risk entries.
- The system explains the probable relationship using shared cause, event, impact, workstream or milestone.
- The output is labelled as a suggestion, not a confirmed duplicate.
- The system does not merge risks automatically.
- The user can choose: merge, link, keep separate, reject suggestion or defer.
- The user must record a reason when merging two risks.

### US-07: Protect Distinct Workstream Risks

**As a Project Manager, I want risks with similar wording but different ownership or impact to remain separate when needed so that accountability is not lost.**

#### Acceptance Criteria

- The comparison view shows workstream, owner, milestone, cause and impact for both risks.
- The user can retain both risks and create a relationship link.
- The system records the reviewer decision and reason.
- The system must not treat a high similarity score as sufficient evidence for merging.

---

## Epic 4: Challenge Mitigation Quality

### US-08: Generate Mitigation Challenge Questions

**As an NPD Project Manager, I want the system to challenge unclear mitigation actions so that the review meeting focuses on specific preventive decisions.**

#### Acceptance Criteria

- The system compares the mitigation with the recorded cause, event and impact.
- The system identifies missing owner, due date, evidence, trigger or contingency where applicable.
- The system generates a review question rather than declaring the mitigation adequate or inadequate.
- The question must not introduce unsupported project facts.
- The user can accept, edit, reject or defer the question.
- The final mitigation decision remains with the authorised risk owner and Project Manager.

### US-09: Distinguish Mitigation from Contingency

**As a Risk Owner, I want the product to distinguish preventive mitigation from contingency action so that the risk response remains clear.**

#### Acceptance Criteria

- The system can flag when the mitigation appears to describe only a corrective or contingency response.
- The output is presented as a challenge for human review.
- The system does not automatically reclassify the action.
- The user can confirm, correct or reject the finding.

---

## Epic 5: Review Evidence Freshness

### US-10: Flag Potentially Stale Evidence

**As an APQP Coordinator, I want potentially stale supporting evidence to be highlighted so that decisions are not based on outdated information.**

#### Acceptance Criteria

- The MVP uses a provisional, clearly labelled evidence-age rule.
- The system shows the evidence date, review date and reason for the stale-evidence flag.
- A missing evidence date is reported separately from stale evidence.
- The user can classify the evidence as current, outdated, not applicable or requiring follow-up.
- The production evidence-age threshold must be configurable by evidence type and customer policy.

---

## Epic 6: Support Human Review and Accountability

### US-11: Review Every AI Finding

**As an authorised reviewer, I want to control every AI-generated finding so that consequential programme-risk decisions remain human decisions.**

#### Acceptance Criteria

- Every AI finding provides the actions: accept, edit, reject or defer.
- Related-risk findings additionally provide: merge, link or keep separate.
- No AI finding changes the official risk register without human confirmation.
- The reviewer can enter a decision rationale.
- The reviewer identity and timestamp are recorded.
- The product clearly distinguishes deterministic rule results from AI inferences.

### US-12: Escalate Uncertain or High-Impact Cases

**As an APQP Coordinator, I want uncertain or potentially high-impact cases to be escalated so that specialised judgement is obtained when required.**

#### Acceptance Criteria

- The prototype provides an escalation action.
- The reviewer selects or enters the reason for escalation.
- The finding can be assigned to an authorised Project Manager, Quality Manager, Manufacturing Engineering Manager or other configured role.
- The system does not claim that escalation confirms the risk.
- The escalation and final response are included in the audit history.

### US-13: Use a Safe Fallback

**As a Project Manager, I want the monthly review to continue if the AI capability is unavailable so that programme governance does not depend on one model or provider.**

#### Acceptance Criteria

- Deterministic completeness and date checks remain available when the AI service is unavailable, where technically feasible.
- The interface clearly states that semantic AI review is unavailable.
- Uploaded data is not lost.
- The user can continue with manual review.
- The failure is logged for investigation.

---

## Epic 7: Prepare the Review Meeting

### US-14: Generate a Verified Review Agenda

**As an NPD Project Manager, I want a verified review agenda so that the meeting focuses on unresolved decisions rather than register cleaning.**

#### Acceptance Criteria

- Only human-confirmed findings are included in the verified agenda.
- The agenda separates overdue actions, incomplete risks, related-risk decisions, weak mitigation questions and stale evidence.
- Each agenda item includes risk ID, owner, required decision and supporting reason.
- The agenda can be viewed in the prototype.
- The prototype clearly labels any simulated export function.
- The agenda does not approve, close or escalate risks automatically.

---

## Epic 8: Maintain Traceability

### US-15: Record an Audit Trail

**As a programme governance reviewer, I want changes and review decisions to be traceable so that the team can understand how the final register was produced.**

#### Acceptance Criteria

- The audit record includes the original text, finding type, recommendation, human decision, rationale, reviewer and timestamp.
- The audit record identifies whether the finding came from a deterministic rule or AI inference.
- The audit record includes the relevant rule, prompt or model version where available.
- Audit history cannot be silently overwritten in the prototype demonstration.
- Access to audit information should be role controlled in production.

---

## Epic 9: Monitor Product Value and Harm

### US-16: View Evaluation Measures

**As a Product Manager, I want to view product and quality measures so that I can decide whether RiskReview AI should proceed, be reworked or stop.**

#### Acceptance Criteria

- The evaluation view separates technical, product, operational and business measures.
- Technical measures may include duplicate-suggestion precision, reviewer agreement, unsupported-output rate and meaning-change incidents.
- Product measures may include accepted, edited, rejected and deferred findings.
- Operational measures may include processing time and human-review time.
- Business measures may include measured preparation-time change and register-completeness change.
- Synthetic or illustrative metrics are labelled clearly.
- The dashboard does not present unmeasured improvement as a proven result.

---

## Epic 10: Protect Confidentiality and User Control

### US-17: Use Synthetic Data in the Prototype

**As a team member, I want the prototype to use fictional automotive programme-risk data so that confidential customer and supplier information is not exposed.**

#### Acceptance Criteria

- No real customer, supplier, programme, drawing or commercial data is included.
- Fictional organisations and programme identifiers are used.
- The repository states that the data is synthetic.
- Any future pilot using real information requires approved access, purpose limitation, retention and deletion controls.

### US-18: Correct or Contest a Finding

**As a Risk Owner, I want to challenge an incorrect finding so that AI output does not become unreviewed ground truth.**

#### Acceptance Criteria

- The user can reject or edit every AI finding.
- The user can record a correction reason.
- The correction is preserved in the audit trail.
- The original AI finding remains traceable.
- User correction data is not automatically used for model training without an approved process.

---

# Cross-Cutting Acceptance Criteria

The following criteria apply to the entire MVP:

1. All prototype data must be synthetic or fictional.
2. AI findings must be labelled as inferences or suggestions.
3. Deterministic rule findings must be distinguishable from AI findings.
4. No probability, impact, FMEA rating, PPAP approval or Start-of-Production approval may be automated.
5. Every proposed text change must require human confirmation.
6. Severe meaning-change or fabricated-fact incidents must block progression to a wider pilot until resolved.
7. All demonstration thresholds and scores must be labelled provisional.
8. The prototype must provide a manual fallback path.
9. The repository must preserve the AI build prompt, self-evaluation and collaboration log.
10. Requirements may be revised after discovery and usability evidence.

# Definition of Done for This Artifact

This user-story artifact is complete when:

- Every MVP capability is connected to a user outcome.
- Acceptance criteria are testable in the prototype or evaluation process.
- Human decision authority is explicit.
- Out-of-scope consequential automation is excluded.
- Synthetic-data and evidence limitations are transparent.
- Ambiguous requirements are transferred to the discovery or decision log.
