# Executive Summary

## Product Title

**RiskReview AI**

## Industry and Initial Segment

RiskReview AI is designed for the **automotive industry**, initially focusing on **Tier 1 and Tier 2 automotive component manufacturers** executing **New Product Development (NPD)** and **New Product Introduction (NPI)** programmes from **Advanced Product Quality Planning (APQP)** to **Start of Production (SOP)**.

## Business Problem

Automotive component programmes involve several interdependent workstreams, including customer requirements, design, tooling, supplier readiness, manufacturing engineering, validation, quality planning, Production Part Approval Process (PPAP), capacity readiness and production launch.

Programme risks are entered by different risk owners using different writing styles and levels of detail. Risk entries may have missing owners or dates, weak cause-event-impact structure, duplicated concerns, stale supporting evidence or mitigation actions that do not clearly address the stated cause. Consequently, monthly programme-risk and launch-readiness meetings may spend significant time correcting and interpreting the risk register instead of making preventive decisions.

## Proposed Product

RiskReview AI is a **human-supervised AI copilot** that reviews the quality and readiness of an automotive programme risk register before the monthly review meeting.

The product combines:

1. Deterministic checks for mandatory fields, ownership, dates and overdue actions
2. AI-assisted review of cause-event-impact structure
3. Suggestions for potentially related or duplicate risks
4. Mitigation challenge questions
5. Evidence-freshness indicators
6. Human accept, edit, reject, link, merge or defer actions
7. Verified review-agenda generation
8. Decision and audit-history recording

## Why AI Is Required

Rules are suitable for objective checks such as missing fields, invalid dates and overdue actions. However, rules alone cannot reliably interpret whether two differently worded risks refer to the same underlying concern, whether a mitigation addresses the stated cause, or whether a risk statement clearly separates cause, uncertain event and impact.

AI is therefore used only for semantic review and decision support. Authorised humans remain responsible for probability, impact, mitigation selection, acceptance, escalation, merging and closure.

## Primary Users and Buyer

- **Primary users:** NPD Project Manager and APQP Coordinator
- **Supporting users:** Risk owners, Quality, Supplier Quality, Tooling, Manufacturing Engineering, Procurement, Validation and Logistics teams
- **Potential economic buyer:** Automotive component manufacturer, programme leadership or Project Management Office

## Minimum Viable Product

The initial MVP will cover:

- One fictional automotive component programme
- One standard risk-register format
- APQP to Start of Production
- English-language risk entries
- Synthetic automotive programme-risk data
- Monthly risk-review preparation
- Human confirmation for every AI-generated finding

The MVP will not assign risk probability or impact, replace DFMEA or PFMEA, assign FMEA ratings, approve PPAP, approve Start of Production, or automatically accept, merge, escalate, close or delete risks.

## Prototype and Evaluation Approach

The prototype will demonstrate risk-register upload, completeness checks, semantic quality findings, related-risk comparison, mitigation challenges, human decisions, verified agenda generation and an audit trail.

The initial evaluation will use fictional automotive programme-risk data and compare manual review with AI-assisted review. Key measures will include:

- Duplicate-suggestion precision and recall
- Agreement with human reviewers
- Useful-finding rate
- Unsupported-suggestion rate
- Changed-meaning incidents
- Human correction effort
- Review-preparation time
- Processing cost per register

All prototype results will be labelled as synthetic, illustrative or provisional until validated with target users.

## Responsible AI and Governance

RiskReview AI will use role-based human control, side-by-side display of original and suggested text, correction and rejection options, version tracking, audit history, manual fallback and launch blockers for fabricated facts, changed risk meaning, confidentiality failure or unauthorised automated decisions.

## MVP-to-Revenue Direction

The proposed commercial path is:

**Discovery → Clickable Prototype → Controlled MVP Pilot → First Paid Pilot → Annual B2B Subscription → Expansion to Additional Automotive Programmes**

The first commercial offer will be a fixed-scope paid pilot for one automotive component programme. Final pricing will be determined only after buyer and willingness-to-pay interviews.

## Current Recommendation

Team004 recommends proceeding with a narrow prototype and discovery validation. Wider deployment should be considered only after demonstrating useful findings, manageable human-review effort, acceptable cost-to-serve, preserved risk meaning and adequate confidentiality controls.

## Evidence Status

The current assignment uses synthetic data and provisional assumptions. Discovery interviews, usability testing, measured evaluation results and willingness-to-pay evidence remain pending and will be added as the project progresses.
