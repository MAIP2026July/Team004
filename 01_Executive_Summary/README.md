# Team004: RiskReview AI

## 1. Project Overview

**RiskReview AI** is a human-supervised AI copilot for reviewing programme-level risk registers used in automotive component New Product Development (NPD) and New Product Introduction (NPI) programmes.

The initial product is designed for **Tier 1 and Tier 2 automotive component manufacturers** and focuses on the repeated monthly programme-risk and launch-readiness review from **Advanced Product Quality Planning (APQP)** to **Start of Production (SOP)**.

The product helps teams identify incomplete, unclear, duplicated, unsupported, or weakly mitigated risk entries before review meetings. It supports human decision-making but does not replace authorised programme, quality, or launch-approval personnel.

---

## 2. Team Members

| Team Member | BITS ID | GitHub ID |
|---|---|---|
| Maharshi Pandit | 2025MB26121 | [2025mb26121-hub](https://github.com/2025mb26121-hub) |
| Swaminathan B. | 2025MB26109 | [007india](https://github.com/007india) |

---

## 3. Industry and Product Scope

| Area | Selected Scope |
|---|---|
| Industry | Automotive |
| Customer Segment | Tier 1 and Tier 2 automotive component manufacturers |
| Programme Type | NPD and NPI programmes |
| Lifecycle | APQP to SOP |
| Primary Users | NPD Project Manager and APQP Coordinator |
| Initial Workflow | Monthly programme-risk and launch-readiness review |
| Product Type | Human-supervised AI copilot |

---

## 4. Business Problem

Automotive development programmes involve interdependent workstreams such as product design, tooling, supplier readiness, manufacturing engineering, quality, validation, Production Part Approval Process (PPAP), and production launch.

Risk-register entries may be created by different owners using inconsistent formats and varying levels of detail. Before a monthly review, programme teams may need to manually identify:

- Missing owners, dates, actions, or evidence
- Weak cause-event-impact statements
- Overdue mitigation actions
- Potentially related or duplicate risks
- Stale supporting evidence
- Mitigation actions that are vague or not verifiable
- Risks requiring discussion during the review meeting

This manual preparation can reduce the time available for decision-making and may allow important data-quality issues to remain unnoticed.

---

## 5. Proposed Solution

RiskReview AI reviews a programme risk register and produces a traceable, human-verifiable review output.

### MVP capabilities

1. Check mandatory fields and overdue actions using deterministic rules.
2. Review cause-event-impact structure.
3. Identify unclear or incomplete risk descriptions.
4. Suggest potentially related or duplicate risks for human review.
5. Challenge weak mitigation actions with focused questions.
6. flag stale or missing supporting evidence.
7. Generate a verified review agenda linked to source risk IDs.
8. Record user acceptance, rejection, and edits for audit and evaluation.

### Human-control boundary

RiskReview AI does **not**:

- Automatically assign probability or impact
- Assign Failure Mode and Effects Analysis (FMEA) severity, occurrence, or detection ratings
- Replace Design FMEA or Process FMEA
- Approve PPAP
- Approve SOP or launch readiness
- Accept, escalate, merge, close, or delete a risk without authorised human confirmation
- Present AI-generated output as verified fact without source evidence

---

## 6. Why AI Is Used

Deterministic rules are appropriate for exact checks such as missing fields, invalid dates, and overdue actions. AI is used only where language understanding or similarity assessment is needed, including:

- Interpreting cause-event-impact structure
- Identifying potentially related risk narratives
- Evaluating whether mitigation wording is specific and verifiable
- Generating review questions grounded in the supplied risk data
- Summarising selected findings into a review agenda

All AI suggestions remain reviewable and reversible.

---

## 7. Prototype Workflow

1. The user loads or selects a sample risk register.
2. Deterministic checks validate mandatory fields, dates, and overdue actions.
3. AI-assisted checks review narrative quality, related risks, mitigation wording, and evidence freshness.
4. Each finding displays its source risk ID and reason.
5. The user accepts, rejects, or edits the suggestion.
6. Confirmed findings are included in the review agenda.
7. The interaction is recorded for audit and evaluation.

> The prototype is a decision-support demonstration. It is not connected to a live automotive production system and must not be used for real launch-approval decisions.

---

## 8. Repository Structure

```text
TEAM004_RiskReview_AI/
|
|-- README.md
|-- 01_Executive_Summary/
|-- 02_Product_Strategy/
|-- 03_PM_Artifacts/
|-- 04_UX_Workflow_Trust/
|-- 05_Data_Model_Evaluation/
|-- 06_Business_Economics_Scaling/
|-- 07_Ethics_Governance_Risk/
|-- 08_AI_Collaboration/
|-- 09_Prototype/
`-- 10_Presentation/
```

### Folder guide

| Folder | Purpose |
|---|---|
| `01_Executive_Summary` | Concise summary of the problem, product, users, MVP, controls, and recommendation |
| `02_Product_Strategy` | Discovery plan, product vision, Jobs to Be Done, AI opportunities, MVP scope, build/buy/API decisions, and roadmap |
| `03_PM_Artifacts` | Product requirements, personas, user stories, acceptance criteria, prioritisation, and success metrics |
| `04_UX_Workflow_Trust` | Current and future workflows, PlantUML diagrams, wireframes, human-control points, and trust design |
| `05_Data_Model_Evaluation` | Data schema, synthetic inputs, evaluation cases, metrics, error analysis, and prototype test evidence |
| `06_Business_Economics_Scaling` | Buyer, value hypothesis, pilot design, pricing assumptions, unit economics, and scaling approach |
| `07_Ethics_Governance_Risk` | Responsible AI controls, risk register, privacy, security, auditability, and governance |
| `08_AI_Collaboration` | AI-use log, prompts, verification process, reflection, and AI self-evaluation |
| `09_Prototype` | Working prototype, sample data, application files, instructions, screenshots, and test results |
| `10_Presentation` | Final presentation and supporting presentation material |

---

## 9. Prototype Use

Open the `09_Prototype` folder and follow its local `README.md` for the exact run instructions.

For a browser-based prototype, the normal demonstration flow is:

1. Open `index.html` in a modern web browser.
2. Load or select the provided synthetic risk data.
3. Run the review checks.
4. Open each finding and verify its source risk ID.
5. Accept, reject, or edit suggestions.
6. Review the generated meeting agenda.

Only synthetic or properly anonymised data should be used in the assignment prototype.

---

## 10. Evaluation Approach

The prototype should be evaluated using a labelled synthetic test set that includes normal cases and difficult edge cases. Evaluation covers:

- Mandatory-field detection accuracy
- Overdue-action detection accuracy
- Cause-event-impact review quality
- Related-risk suggestion precision
- Mitigation-challenge usefulness
- Evidence-freshness detection
- Source traceability
- Unsupported-claim rate
- User acceptance, rejection, and edit behaviour
- Agenda completeness and correctness

AI-generated outputs must be checked against the original risk records. Test results should clearly distinguish observed evidence from assumptions or future targets.

---

## 11. Responsible AI and Governance

The design applies the following controls:

- Human approval for consequential actions
- Source-linked findings and traceability
- Clear separation of rules, AI suggestions, and human decisions
- No autonomous risk scoring or launch approval
- Role-based access as a production requirement
- Minimal data collection and retention
- Use of synthetic or anonymised assignment data
- Audit logging for accepted, rejected, and edited outputs
- Version control for prompts, rules, and evaluation datasets
- Clear uncertainty and limitation statements

---

## 12. Commercial MVP Direction

The recommended commercial path is a limited paid pilot with one automotive component programme team. Before broader deployment, the team must validate:

- Frequency and cost of manual risk-review preparation
- Availability and quality of risk-register data
- User trust in source-linked AI suggestions
- Improvement in review preparation time and finding quality
- Integration requirements for existing programme-management tools
- Buyer, budget owner, procurement, security, and data-governance requirements
- Willingness to pay using real customer evidence

Commercial assumptions in this repository are hypotheses until validated through interviews or pilot evidence.

---

## 13. Evidence Status

This repository contains assignment research, product-management artefacts, synthetic data, prototype outputs, and evaluation material. Unless a file states otherwise:

- Customer needs are hypotheses requiring discovery validation.
- Performance claims are limited to the documented test set.
- Financial values are planning assumptions, not proven market facts.
- Prototype results do not establish production readiness.
- Live automotive data and real operational approvals are outside the assignment scope.

---

## 14. Academic and AI-Use Declaration

Generative AI was used to support ideation, drafting, structuring, prototype development, synthetic data preparation, and review. Team members remain responsible for:

- Defining the product scope
- Verifying technical and business claims
- Checking consistency across deliverables
- Testing prototype behaviour
- Recording limitations and corrections
- Making final product-management decisions

Detailed prompts, verification steps, corrections, and reflections are documented in `08_AI_Collaboration`.

---

## 15. Current Status

The repository is organised as a complete product-management assignment pack containing strategy, PM artefacts, workflow and trust design, data and evaluation, business analysis, governance, AI-collaboration evidence, prototype material, and the final presentation.

The recommended next step is to upload and verify each folder sequentially, beginning with `01_Executive_Summary`.
