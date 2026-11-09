# # Team004: RiskReview AI

## Team Members

| Team Member | BITS ID | GitHub ID |
|---|---|---|
| Maharshi Pandit | 2025MB26121 | [2025mb26121-hub](https://github.com/2025mb26121-hub) |
| Swaminathan B. | 2025MB26109 | [007india](https://github.com/007india) |

## Product Scope

- **Industry:** Automotive
- **Customer Segment:** Tier 1 and Tier 2 automotive component manufacturers
- **Programme Type:** New Product Development and New Product Introduction
- **Lifecycle:** Advanced Product Quality Planning to Start of Production
- **Primary Users:** NPD Project Manager and APQP Coordinator
- **Initial Workflow:** Monthly programme-risk and launch-readiness review

## Product Summary

**RiskReview AI** is a human-supervised AI copilot that reviews the quality and readiness of automotive programme risk registers before monthly launch-readiness meetings.

The product identifies:

- Incomplete risk entries
- Weak cause-event-impact structure
- Potentially related or duplicate risks
- Stale supporting evidence
- Missing owners, dates or actions
- Unclear or weak mitigation actions

RiskReview AI does not make final programme-risk decisions. Risk probability, impact, mitigation, acceptance, escalation, merging and closure remain under the control of authorised project personnel.

## Problem Statement

Automotive component New Product Development and New Product Introduction programmes involve multiple workstreams, including design, tooling, supplier readiness, manufacturing engineering, quality, validation, Production Part Approval Process and production launch.

Risk entries are created by different owners and may contain incomplete information, inconsistent wording, duplicated concerns, stale evidence or mitigation actions that do not clearly address the stated cause.

As a result, monthly risk-review meetings may spend substantial time correcting and interpreting the risk register instead of making preventive launch-readiness decisions.

## Product Objective

RiskReview AI will help the Project Manager and APQP Coordinator prepare a more complete and decision-ready programme risk register before the monthly review meeting.

The product will combine:

1. Deterministic completeness checks
2. AI-assisted risk-statement quality review
3. Related-risk suggestions
4. Mitigation challenge questions
5. Evidence-freshness checks
6. Human verification and correction
7. Verified review-agenda generation
8. Decision and audit-history recording

## MVP Scope

The initial MVP will cover:

- One fictional automotive component programme
- One standard risk-register format
- APQP to Start of Production
- English-language risk entries
- Synthetic automotive programme-risk data
- Monthly risk-review preparation
- Human confirmation for every AI-generated finding

### Out of Scope

The MVP will not:

- Assign risk probability or impact automatically
- Replace DFMEA or PFMEA
- Assign FMEA severity, occurrence or detection ratings
- Approve Production Part Approval Process
- Approve Start of Production
- Automatically merge, accept, escalate, close or delete risks
- Use confidential customer or supplier data

## Repository Structure

| Folder | Contents |
|---|---|
| `01_Executive_Summary` | Product and assignment overview |
| `02_Product_Strategy` | Problem, customer, vision, opportunity and commercial roadmap |
| `03_PM_Artifacts` | PRD, user stories, acceptance criteria and prioritisation |
| `04_UX_Workflow_Trust` | Initial PlantUML workflow, user journey and trust design |
| `05_Data_Model_Evaluation` | Data strategy, synthetic dataset, architecture and evaluation |
| `06_Business_Economics_Scaling` | Customer value, pricing, cost-to-serve and scaling |
| `07_Ethics_Governance_Risk` | Responsible AI, privacy, risks and launch blockers |
| `08_AI_Collaboration` | AI product-build prompt, self-g |
| `09_Prototype` | Functional prototype, demo guide and screenshots |
| `10_Presentation` | Presentation outline, contribution statement and references |

## Initial Workflow

The initial swimlane workflow is available in:

04_UX_Workflow_Trust/01_Initial_Workflow_PlantUML.md

The workflow will be revised after discovery interviews, PRD validation and prototype usability evaluation.

## Prototype

The prototype demonstrates:

- Risk-register upload and validation
- Register-quality dashboard
- Individual risk-quality findings
- Related-risk comparison
- Mitigation challenge questions
- Human accept, edit, reject, link, merge or defer actions
- Verified review agenda
- Audit and evaluation dashboard

Prototype instructions are available in:

09_Prototype/README.md

## MVP-to-Revenue Approach

The proposed commercial path is:

```text
Discovery
→ Clickable Prototype
→ Controlled MVP Pilot
→ First Paid Pilot
→ Annual B2B Subscription
→ Expansion to Additional Automotive Programmes
