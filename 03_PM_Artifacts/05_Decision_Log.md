# RiskReview AI: Product Decision Log

## Document Purpose

This decision log records the major product decisions made by Team004 for RiskReview AI. It explains what was decided, why the decision was made, the alternatives considered, the evidence available at the time, and what may cause the team to revisit the decision.

The log is intended to preserve traceability across the Product Requirements Document, prototype, evaluation plan, business case, and final presentation.

## Decision Status

- **Proposed:** Decision is under discussion.
- **Accepted:** Decision is approved for the current assignment stage.
- **Superseded:** A later decision has replaced the original decision.
- **Deferred:** Decision is intentionally postponed until more evidence is available.
- **Rejected:** Alternative was considered but not selected.

---

## Decision 001: Select a Specific Automotive Segment

- **Status:** Accepted
- **Decision:** Focus RiskReview AI on Tier 1 and Tier 2 automotive component manufacturers executing New Product Development and New Product Introduction programmes.
- **Lifecycle Boundary:** Advanced Product Quality Planning to Start of Production.
- **Primary Workflow:** Monthly programme-risk and launch-readiness review.
- **Reason:** The professor instructed teams to begin with a specific industry and segment rather than a cross-industry product. Automotive component programmes provide a repeated cross-functional risk-review workflow with clear milestones, users, and governance decisions.
- **Alternatives Considered:** Cross-industry project risk management; renewable-energy construction; automotive warranty claims; predictive maintenance.
- **Why Alternatives Were Not Selected:** Cross-industry scope was too broad. The other alternatives would change the approved programme-risk-review problem or require different datasets and users.
- **Revisit Trigger:** Discovery evidence shows that the selected users do not experience the proposed problem frequently or do not see sufficient value.

## Decision 002: Define the Primary Users

- **Status:** Accepted
- **Decision:** The NPD Project Manager and APQP Coordinator are the primary users. Risk owners, Quality Managers, Manufacturing Engineering, Supplier Quality, Procurement, Tooling, Logistics, and Validation teams are supporting users.
- **Reason:** The primary users coordinate the programme risk register and prepare launch-readiness reviews, while supporting users contribute evidence and mitigation actions.
- **Alternative Considered:** Treat all project stakeholders as equal primary users.
- **Why Not Selected:** A broad user definition would create unclear product requirements and an unfocused interface.
- **Revisit Trigger:** Discovery interviews identify a different role as the actual workflow owner or economic decision-maker.

## Decision 003: Position RiskReview AI as a Human-Supervised Copilot

- **Status:** Accepted
- **Decision:** RiskReview AI will support risk-register quality review and meeting preparation. Authorised humans will retain all consequential programme-risk decisions.
- **Human-Controlled Decisions:** Probability, impact, mitigation selection, risk acceptance, escalation, merging, closure, PPAP approval, and Start-of-Production approval.
- **Reason:** AI can assist with semantic review and pattern identification, but programme-risk decisions require context, accountability, and domain judgement.
- **Alternative Considered:** Autonomous risk scoring and automated closure.
- **Why Not Selected:** The alternative creates unacceptable governance, traceability, and over-reliance risks for the MVP.
- **Revisit Trigger:** None for automatic approvals in the current product boundary. Any future authority increase would require new evidence, governance approval, and controlled testing.

## Decision 004: Separate Deterministic Rules from AI Capabilities

- **Status:** Accepted
- **Decision:** Use deterministic rules for objective checks and AI only for tasks requiring semantic interpretation.
- **Deterministic Checks:** Missing mandatory fields, invalid dates, overdue actions, missing owners, and evidence-age thresholds.
- **AI-Assisted Tasks:** Cause-event-impact review, potentially related-risk suggestions, mitigation challenge questions, and controlled agenda drafting.
- **Reason:** Rules are more reliable, testable, and explainable for fixed conditions. AI adds value where wording, context, and semantic similarity matter.
- **Alternative Considered:** Use a language model for every validation task.
- **Why Not Selected:** This would increase cost and variability without improving objective checks.
- **Revisit Trigger:** A rule becomes too complex or context-dependent to remain dependable, or a configurable business-rule engine becomes necessary.

## Decision 005: Preserve the Boundary with Automotive Core Tools

- **Status:** Accepted
- **Decision:** RiskReview AI will not replace DFMEA, PFMEA, Control Plan, MSA, SPC, or PPAP processes.
- **Reason:** These tools address specific product and process quality requirements. RiskReview AI addresses the wider programme-level risk register and launch-readiness review.
- **Alternative Considered:** Include automatic FMEA scoring and PPAP approval in the product.
- **Why Not Selected:** The alternative is outside the problem scope and introduces additional technical and governance risk.
- **Revisit Trigger:** None for the MVP. Future integrations may reference approved evidence without taking over formal quality decisions.

## Decision 006: Use Synthetic Automotive Data for the Prototype

- **Status:** Accepted
- **Decision:** Build and demonstrate the prototype using fictional or synthetic automotive programme-risk entries.
- **Reason:** Real programme data may contain confidential customer, supplier, design, quality, and commercial information. Synthetic data allows safe development and evaluation of the workflow.
- **Alternative Considered:** Use real project risk registers immediately.
- **Why Not Selected:** Governance approval, access controls, data minimisation, and confidentiality arrangements are not yet available.
- **Revisit Trigger:** A controlled pilot receives formal approval to use de-identified or access-controlled real data.

## Decision 007: Make Every AI Finding Contestable

- **Status:** Accepted
- **Decision:** Users must be able to accept, edit, reject, link, merge, keep separate, or defer findings, with a reason recorded where appropriate.
- **Reason:** AI findings may be incomplete or contextually wrong. Contestability protects meaning, accountability, and user trust.
- **Alternative Considered:** Display findings without correction controls.
- **Why Not Selected:** This would encourage passive acceptance and weaken the feedback and audit process.
- **Revisit Trigger:** Usability testing shows that the decision set needs simplification or role-specific controls.

## Decision 008: Require Evidence and Auditability

- **Status:** Accepted
- **Decision:** Each finding should show the original text, finding type, reason or evidence, confidence or uncertainty, model/prompt/rule version, human action, reviewer, timestamp, and final verified text.
- **Reason:** The product must support traceability and allow decisions to be reviewed later.
- **Alternative Considered:** Store only the final edited risk register.
- **Why Not Selected:** The alternative would remove the history needed to understand AI influence and human accountability.
- **Revisit Trigger:** Customer governance requirements demand additional fields or retention controls.

## Decision 009: Use a Narrow MVP

- **Status:** Accepted
- **Decision:** The MVP will cover one fictional automotive component programme, one risk-register format, English-language entries, and the monthly pre-review workflow.
- **Included:** Completeness checks, semantic quality review, related-risk suggestions, mitigation challenges, stale-evidence flags, human decisions, verified agenda, and audit trail.
- **Reason:** A narrow MVP can test the central value hypothesis without creating a broad enterprise platform.
- **Alternative Considered:** Multi-programme, multilingual, fully integrated enterprise product.
- **Why Not Selected:** The alternative would increase effort before validating user value.
- **Revisit Trigger:** The narrow workflow demonstrates usefulness, acceptable correction effort, and manageable cost-to-serve.

## Decision 010: Use a Paid Pilot as the First Commercial Step

- **Status:** Accepted
- **Decision:** After prototype validation, offer a fixed-scope paid pilot for one automotive component programme before proposing an annual subscription.
- **Reason:** A paid pilot tests buyer commitment, onboarding effort, workflow fit, cost-to-serve, and measurable value with limited exposure.
- **Alternative Considered:** Launch a full annual subscription immediately or provide an unlimited free pilot.
- **Why Not Selected:** The subscription would be premature, while a free pilot may not validate willingness to pay.
- **Pricing Status:** Deferred until buyer interviews and cost-to-serve analysis are completed.
- **Revisit Trigger:** Discovery identifies a different preferred procurement model.

## Decision 011: Maintain PM Artifacts in Markdown on GitHub

- **Status:** Accepted
- **Decision:** Product Management artifacts will be maintained as Markdown files in the Team004 GitHub repository.
- **Reason:** The professor requested GitHub submission and preferably Markdown PM artifacts. Markdown also enables version history, review, and traceability.
- **Alternative Considered:** Use only Word and PDF files.
- **Why Not Selected:** Static documents provide weaker change history and repository navigation.
- **Revisit Trigger:** Formal submission instructions require an additional PDF or presentation version.

## Decision 012: Use PlantUML for the Initial Swimlane Workflow

- **Status:** Accepted
- **Decision:** Document the initial workflow using PlantUML and revise it after discovery and usability testing.
- **Reason:** The professor specifically requested an initial swimlane and recommended PlantUML. Text-based diagrams can be version controlled with the other artifacts.
- **Alternative Considered:** Use only a static image or prose description.
- **Why Not Selected:** Static images are harder to review and update, while prose alone does not clearly show roles and handoffs.
- **Revisit Trigger:** Discovery changes roles, handoffs, escalation paths, or system boundaries.

## Decision 013: Ask AI to Build and Self-Evaluate the Prototype

- **Status:** Accepted
- **Decision:** Provide the PM artifacts to an AI tool with two requests: build a product prototype and critically self-evaluate the result.
- **Required Self-Evaluation:** Feedback, ambiguity, recommended changes, hard-coded items, configurable items, risks, and unsupported claims.
- **Reason:** This directly follows the professor's WhatsApp instruction and demonstrates critical AI collaboration rather than unreviewed content generation.
- **Alternative Considered:** Use AI only for writing support.
- **Why Not Selected:** The assignment explicitly asks for AI-assisted product building and self-evaluation.
- **Revisit Trigger:** AI output exposes additional ambiguities or changes the feasible prototype scope.

## Decision 014: Treat Prototype Results as Illustrative Until Measured

- **Status:** Accepted
- **Decision:** Label prototype scores, confidence values, dashboard metrics, time savings, and commercial values as synthetic, illustrative, provisional, or TBD until measured.
- **Reason:** The team must not fabricate interviews, user results, accuracy, financial outcomes, or willingness to pay.
- **Alternative Considered:** Present assumed performance as achieved results.
- **Why Not Selected:** This would weaken academic integrity and evidence quality.
- **Revisit Trigger:** Replace provisional values only after genuine testing and documented evidence.

---

## Deferred Decisions

The following decisions remain open until evidence is collected:

1. Final economic buyer and procurement owner
2. Production deployment architecture
3. Model or API provider
4. Final similarity and confidence thresholds
5. Evidence-freshness periods by risk category
6. Paid-pilot price
7. Subscription pricing unit
8. Integration with customer risk-management or APQP systems
9. Data-retention period
10. Final pilot acceptance thresholds

## Decision Review Process

The team will review the decision log when:

- Discovery interviews are completed
- The PRD is reviewed by target users
- The prototype is generated by AI
- The AI self-evaluation is received
- Usability testing is completed
- Evaluation results become available
- Commercial interviews are completed
- The final recommendation is prepared

Any changed decision should be added as a new entry. The earlier decision should remain visible and be marked **Superseded** rather than deleted.

## Ownership

- **Maharshi Pandit:** Prototype, workflow, dataset, evaluation, metrics, and decision-traceability updates
- **Swaminathan B.:** Discovery, customer validation, strategy, economics, roadmap, and commercial-decision updates
- **Joint Ownership:** Product boundaries, responsible AI, launch blockers, final recommendation, and approval of all material decision changes

## Evidence Status

This log records the team's current product decisions. Decisions based on assumptions must be validated through discovery, prototype testing, controlled evaluation, and buyer research before being treated as final production decisions.
