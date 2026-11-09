# Product Backlog

## 1. Purpose

This backlog converts the RiskReview AI Product Requirements Document, user stories and feature priorities into an ordered delivery plan for the clickable prototype and controlled MVP.

The backlog applies to:

- **Industry:** Automotive
- **Segment:** Tier 1 and Tier 2 automotive component manufacturers
- **Programme:** New Product Development and New Product Introduction
- **Lifecycle:** Advanced Product Quality Planning to Start of Production
- **Primary Users:** NPD Project Manager and APQP Coordinator
- **Workflow:** Monthly programme-risk and launch-readiness review

## 2. Backlog Scoring Method

Each backlog item is assessed using:

- **Priority:** Must, Should, Could or Not Now
- **User Value:** 1 to 5
- **Risk Reduction:** 1 to 5
- **Effort:** Small, Medium or Large
- **Dependency:** Earlier work required before implementation
- **Evidence Status:** Assumption, validated need or measured result

Current scores are provisional and must be updated after discovery and usability testing.

## 3. Ordered MVP Backlog

| ID | Backlog Item | Priority | User Value | Risk Reduction | Effort | Dependency | Prototype Release |
|---|---|---:|---:|---:|---|---|---|
| PB-01 | Define synthetic automotive programme and standard risk-register schema | Must | 5 | 5 | Medium | None | V0.1 |
| PB-02 | Upload and validate CSV risk register | Must | 5 | 4 | Medium | PB-01 | V0.1 |
| PB-03 | Check mandatory fields and invalid values | Must | 5 | 5 | Small | PB-01 | V0.1 |
| PB-04 | Check overdue actions and review dates | Must | 5 | 4 | Small | PB-01 | V0.1 |
| PB-05 | Display register-quality dashboard | Must | 5 | 3 | Medium | PB-02 to PB-04 | V0.1 |
| PB-06 | Review cause-event-impact structure | Must | 5 | 5 | Large | Dataset and rubric | V0.2 |
| PB-07 | Show original and suggested risk text side by side | Must | 5 | 5 | Medium | PB-06 | V0.2 |
| PB-08 | Generate mitigation challenge questions | Must | 5 | 4 | Large | PB-06 | V0.2 |
| PB-09 | Flag potentially stale evidence | Must | 4 | 4 | Small | PB-01 | V0.2 |
| PB-10 | Capture accept, edit, reject and defer actions | Must | 5 | 5 | Medium | PB-06 to PB-09 | V0.2 |
| PB-11 | Suggest potentially related risks | Should | 4 | 4 | Large | Labelled pair dataset | V0.3 |
| PB-12 | Support link, merge and keep-separate decisions | Should | 4 | 5 | Medium | PB-11 | V0.3 |
| PB-13 | Generate verified review agenda | Must | 5 | 4 | Medium | PB-10 and PB-12 | V0.3 |
| PB-14 | Record audit history and version information | Must | 5 | 5 | Medium | All findings | V0.3 |
| PB-15 | Provide rules-only and manual fallback | Should | 5 | 5 | Medium | PB-03 to PB-04 | V0.3 |
| PB-16 | Show evaluation dashboard with synthetic labels | Should | 4 | 4 | Medium | Evaluation plan | V0.3 |
| PB-17 | Export verified agenda | Should | 3 | 2 | Small | PB-13 | Pilot |
| PB-18 | Add configurable automotive taxonomy | Should | 4 | 3 | Medium | Discovery | Pilot |
| PB-19 | Add role-based access | Must for pilot | 5 | 5 | Large | Security design | Pilot |
| PB-20 | Add monitoring and incident controls | Must for pilot | 5 | 5 | Large | Production architecture | Pilot |

## 4. Prototype Release Plan

### Version 0.1: Deterministic Foundation

**Goal:** Demonstrate a usable automotive risk-register review starting point.

Included:

- Synthetic automotive programme setup
- CSV upload
- File and column validation
- Mandatory-field checks
- Invalid-date and overdue-action checks
- Dashboard summary
- Clear synthetic-data labelling

**Exit criteria:**

- Approved sample CSV loads successfully.
- Required-field checks match the reference test cases.
- Errors identify the affected risk ID and field.
- No uploaded row is silently removed or rewritten.

### Version 0.2: Human-Supervised Semantic Review

**Goal:** Demonstrate AI-assisted review without transferring decision authority.

Included:

- Cause-event-impact review
- Original-versus-suggested comparison
- Mitigation challenge questions
- Stale-evidence findings
- Accept, edit, reject and defer controls
- Finding explanations

**Exit criteria:**

- Every AI finding displays original text and rationale.
- Every proposed text change requires explicit human confirmation.
- Users can reject or correct findings.
- No probability, impact or launch decision is automated.

### Version 0.3: Review Decision and Audit

**Goal:** Complete the pre-review workflow.

Included:

- Potentially related-risk suggestions
- Side-by-side risk comparison
- Link, merge or keep-separate decisions
- Verified review agenda
- Audit history
- Manual fallback
- Evaluation dashboard

**Exit criteria:**

- No risk is merged automatically.
- Only verified findings enter the review agenda.
- Every human decision records reviewer, reason, timestamp and version.
- The full upload-to-agenda workflow can be demonstrated.

## 5. Discovery Backlog

| ID | Discovery Item | Owner | Output | Status |
|---|---|---|---|---|
| DB-01 | Interview NPD Project Manager | Team004 | Current workflow and pain points | Pending |
| DB-02 | Interview APQP Coordinator | Team004 | Required fields, stages and evidence | Pending |
| DB-03 | Interview Quality or PPAP stakeholder | Team004 | Governance and milestone needs | Pending |
| DB-04 | Interview Manufacturing Engineering stakeholder | Team004 | Workstream terminology and risk examples | Pending |
| DB-05 | Identify economic buyer | Team004 | Pilot approval and funding path | Pending |
| DB-06 | Measure manual preparation baseline | Team004 | Time and rework baseline | Pending |
| DB-07 | Validate willingness to test prototype | Team004 | Usability test participants | Pending |
| DB-08 | Validate willingness to pay | Team004 | Paid-pilot evidence | Pending |

No discovery item should be marked complete until genuine evidence has been collected.

## 6. Data and Evaluation Backlog

| ID | Data or Evaluation Item | Priority | Status |
|---|---|---:|---|
| DE-01 | Define final synthetic risk-register schema | Must | Pending |
| DE-02 | Create at least 60 fictional automotive risks | Must | Pending |
| DE-03 | Create true and false related-risk pairs | Must for PB-11 | Pending |
| DE-04 | Create clear and vague cause-event-impact examples | Must | Pending |
| DE-05 | Create strong and weak mitigation examples | Must | Pending |
| DE-06 | Prepare human labelling guide | Must | Pending |
| DE-07 | Label development set independently | Must | Pending |
| DE-08 | Resolve reviewer disagreement | Must | Pending |
| DE-09 | Preserve held-out evaluation set | Must | Pending |
| DE-10 | Run manual-versus-assisted timed test | Must before pilot | Pending |
| DE-11 | Calculate technical and product measures | Must before pilot | Pending |
| DE-12 | Document unsupported and meaning-change incidents | Must | Pending |

## 7. Governance Backlog

| ID | Governance Item | Priority | Status |
|---|---|---:|---|
| GB-01 | Define human authority matrix | Must | Draft required |
| GB-02 | Define confidential-data boundary | Must | Draft required |
| GB-03 | Define retention and deletion policy | Must for pilot | Pending |
| GB-04 | Define launch blockers | Must | Draft required |
| GB-05 | Define model, rule and prompt versioning | Must | Pending |
| GB-06 | Define incident response and rollback | Must for pilot | Pending |
| GB-07 | Test writing-style bias | Must before pilot | Pending |
| GB-08 | Define user correction and appeal path | Must | Pending |
| GB-09 | Define provider outage fallback | Must | Pending |
| GB-10 | Complete AI self-evaluation | Must for assignment | Pending |

## 8. Commercial Backlog

| ID | Commercial Item | Stage | Status |
|---|---|---|---|
| CB-01 | Identify economic buyer | Discovery | Pending |
| CB-02 | Estimate current preparation cost | Discovery | Pending |
| CB-03 | Estimate prototype cost per register | MVP | Pending |
| CB-04 | Test paid-pilot interest | Discovery | Pending |
| CB-05 | Define fixed-scope paid-pilot package | Pre-pilot | Draft required |
| CB-06 | Estimate pilot delivery cost | Pre-pilot | Pending |
| CB-07 | Select recurring pricing unit | After pilot | Pending |
| CB-08 | Validate annual subscription interest | Pilot | Pending |

## 9. Definition of Ready

A backlog item is ready for implementation when:

- The user and outcome are clear.
- Acceptance criteria are testable.
- Required synthetic data or dependencies are available.
- Human authority and product boundary are defined.
- Security and confidentiality assumptions are visible.
- The team understands whether the behaviour is functional, simulated or Wizard-of-Oz.
- Open ambiguity is recorded in the decision log.

## 10. Definition of Done

A backlog item is complete when:

- Acceptance criteria are met.
- The implementation or prototype behaviour is demonstrated.
- Synthetic or simulated behaviour is labelled.
- Relevant tests or evaluation cases have been executed.
- Human-control requirements are preserved.
- Documentation and screenshots are updated.
- The change is committed to GitHub with a meaningful message.
- Any new risk, ambiguity or configuration item is recorded.

## 11. Hard-Coded versus Configurable Items

### Hard-Coded for the Academic Prototype

- Fictional automotive component programme
- Sample APQP stages
- Synthetic risk entries
- Demonstration evidence-age threshold
- Example similarity and confidence values
- Demonstration dashboard counts
- Example user names and audit events

### Configurable in a Production Product

- Mandatory fields
- Risk categories
- APQP stages and customer milestones
- Evidence-age rules
- Review interval
- Similarity threshold
- User roles
- Escalation path
- Notification rules
- Model and provider
- Prompt and rubric version
- Report and agenda format

## 12. Deferred Backlog

The following items are intentionally deferred:

- Automatic probability and impact scoring
- FMEA rating or replacement
- PPAP approval
- Start-of-Production approval
- Automatic risk closure
- Automatic customer escalation
- Warranty prediction
- Portfolio-wide predictive risk modelling
- Live enterprise integration
- Multilingual production support

These items should not be added unless the product boundary is formally reviewed and supported by evidence.

## 13. Current Sprint Recommendation

The first working sprint should complete:

1. DE-01: Synthetic schema
2. PB-01: Programme context
3. PB-02: CSV upload
4. PB-03: Mandatory-field checks
5. PB-04: Date and overdue checks
6. PB-05: Dashboard

The second sprint should focus on PB-06 to PB-10 only after the semantic review rubric and sample data are prepared.

## 14. Current Evidence Status

- Backlog order is based on the current Product Requirements Document and professor instructions.
- Discovery validation is pending.
- Effort estimates are relative, not measured development estimates.
- Commercial priorities remain assumptions until buyer evidence is obtained.
- Prototype metrics must not be presented as achieved production results.
'''

path = Path('/mnt/data/04_Product_Backlog.md')
path.write_text(content, encoding='utf-8')
print(f'Created {path.name} with {len(content.splitlines())} lines and {path.stat().st_size} bytes')
递 = None
# verify key headings
text = path.read_text(encoding='utf-8')
for heading in ['# Product Backlog','## 3. Ordered MVP Backlog','## 9. Definition of Ready','## 10. Definition of Done']:
    assert heading in text
print('Verified key sections')
'} po = None
# Execute corrected portion only above accidental invalid variable? 
# The code is intentionally rebuilt below to avoid syntax issue.
