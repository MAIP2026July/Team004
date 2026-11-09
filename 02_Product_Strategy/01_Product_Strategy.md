# Product Strategy

## 1. Product Title

**RiskReview AI**

## 2. Industry and Initial Segment

- **Industry:** Automotive
- **Customer segment:** Tier 1 and Tier 2 automotive component manufacturers
- **Programme type:** New Product Development (NPD) and New Product Introduction (NPI)
- **Lifecycle boundary:** Advanced Product Quality Planning (APQP) to Start of Production (SOP)
- **Primary users:** NPD Project Manager and APQP Coordinator
- **Initial workflow:** Monthly programme-risk and launch-readiness review

RiskReview AI is intentionally limited to one automotive segment and one repeated workflow. Wider automotive or cross-industry use is treated as a future expansion hypothesis, not as part of the initial MVP.

## 3. Business Problem

Automotive component development programmes involve interdependent workstreams such as customer requirements, design, prototype development, tooling, supplier readiness, manufacturing engineering, validation, quality planning, Production Part Approval Process (PPAP), capacity readiness and production launch.

Programme risks are entered and updated by different risk owners. The entries may contain:

- Missing owners, dates, triggers or evidence
- Vague descriptions without a clear cause, uncertain event and impact
- Similar risks recorded by different functions
- Mitigation actions that do not clearly address the stated cause
- Stale evidence or overdue actions
- Inconsistent terminology across engineering, quality, procurement and manufacturing teams

As a result, monthly risk-review meetings may spend significant time correcting and interpreting the register instead of making preventive launch-readiness decisions.

## 4. Target Customer and Users

### Economic Buyer

The likely economic buyer is the automotive component manufacturer's programme leadership, Project Management Office, quality leadership or digital-transformation function.

### Primary Users

- NPD Project Manager
- APQP Coordinator

### Supporting Users

- Design Engineering
- Manufacturing Engineering
- Quality and Supplier Quality
- Tooling
- Procurement
- Testing and Validation
- Production Planning
- Logistics
- Individual risk owners

### Beneficiaries

- Cross-functional programme team
- Senior programme governance
- Automotive Original Equipment Manufacturer customer receiving the component

## 5. Jobs to Be Done

> When we prepare the monthly programme-risk and launch-readiness review for a new automotive component programme, we want to identify unclear, incomplete, duplicated, stale or weakly controlled risks before the meeting so that the team can focus on preventive decisions, customer milestones, accountable ownership and production-launch readiness.

## 6. Product Vision

Enable automotive programme teams to conduct more focused, evidence-based and accountable risk reviews by improving the quality and readiness of the programme risk register while keeping all consequential programme decisions with authorised people.

## 7. Proposed Product

RiskReview AI is a human-supervised AI copilot that reviews the quality and readiness of an automotive programme risk register before the monthly launch-readiness meeting.

The product will:

1. Validate mandatory fields and dates using deterministic rules.
2. Review whether a risk statement contains a clear cause, uncertain event and impact.
3. Suggest potentially related or duplicate risks using semantic similarity.
4. Generate challenge questions for unclear or weak mitigation actions.
5. Flag evidence that may be stale according to configurable review rules.
6. Present the original text, reason for the finding and supporting evidence.
7. Allow authorised users to accept, edit, reject, link, merge or defer each finding.
8. Generate a verified review agenda after human confirmation.
9. Record the finding, user decision, rationale, reviewer, version and timestamp.

## 8. Why AI Is Required

A mixed product design is proposed because not every problem requires AI.

### Deterministic Rules

Rules are suitable for:

- Missing mandatory fields
- Missing owner or action owner
- Missing or invalid dates
- Overdue actions
- Invalid status values
- Evidence-age checks based on an approved interval

### AI-Assisted Capabilities

AI is useful for:

- Understanding cause-event-impact structure in varied business language
- Finding semantically related risks written with different wording
- Assessing whether mitigation text appears connected to the stated cause or impact
- Drafting contextual challenge questions
- Producing a review-agenda draft from human-verified findings

### Human Decisions

Authorised programme personnel remain responsible for:

- Risk meaning
- Probability and impact
- Mitigation selection
- Risk acceptance
- Escalation
- Merging or linking risks
- Risk closure
- PPAP approval
- Start-of-Production approval

## 9. Alternatives Considered

### Manual Review

Manual review understands programme context but is time-consuming, inconsistent and dependent on reviewer experience.

### Spreadsheet Validation

Spreadsheet rules can identify missing fields and overdue dates, but cannot reliably understand semantic quality, related meaning or mitigation relevance.

### Generic Writing Assistant

A generic writing assistant may improve grammar but may not preserve programme-risk meaning, automotive context, traceability or governance boundaries.

### Proposed Choice

RiskReview AI combines deterministic checks, context-grounded AI assistance and accountable human review. This provides more value than a rules-only tool without delegating consequential programme-risk decisions to AI.

## 10. First Wedge

The first wedge is:

> Monthly pre-review quality assessment of one standard programme risk register for one fictional automotive component NPD/NPI programme from APQP to Start of Production.

This wedge is narrow enough to prototype and evaluate while still delivering a complete and useful workflow outcome.

## 11. Minimum Viable Product Scope

The MVP will include:

- One fictional automotive component programme
- One standard risk-register template
- 30 to 60 synthetic programme-risk entries
- English-language entries
- APQP to Start of Production lifecycle stages
- Deterministic completeness checks
- Cause-event-impact quality review
- Potentially related-risk suggestions
- Mitigation challenge questions
- Evidence-freshness flags
- Human accept, edit, reject, link, merge or defer controls
- Verified review-agenda generation
- Audit history

### Out of Scope

The MVP will not:

- Assign probability or impact automatically
- Replace Design FMEA or Process FMEA
- Assign FMEA severity, occurrence or detection ratings
- Approve PPAP
- Approve Start of Production
- Predict warranty failure
- Automatically accept, escalate, close, merge or delete risks
- Integrate with every enterprise system
- Use confidential customer or supplier data

## 12. Build, Buy and API Strategy

The recommended approach is hybrid.

### Build Internally

- Automotive programme-risk schema
- Deterministic validation rules
- User workflow
- Human-decision controls
- Audit trail
- Product-specific prompts and grounding
- Evaluation dataset and acceptance criteria

### Use Approved External or Local AI Capability

- Text embeddings for semantic similarity
- Language-model support for structured review and challenge-question drafting

### Strategic Control

The product should keep model access behind an internal interface so that the provider can be replaced. The team should maintain an independent evaluation set, version prompts and rules, and provide a rules-only or manual fallback.

## 13. Value Proposition

### User Value

- Less time spent cleaning and interpreting the risk register
- Clearer review agenda
- Better visibility of missing ownership, weak mitigation and stale evidence
- Easier comparison of potentially related risks
- Traceable human decisions

### Business Value

- Reduced review-preparation effort
- More decision-focused governance meetings
- Better action ownership
- Improved launch-readiness visibility
- Reusable programme-risk review process

The product should not claim that it directly prevents every project loss. The initial value claim is improved risk-register quality, preparation efficiency and decision readiness.

## 14. Success Measures

Initial provisional measures include:

### Model and Rule Measures

- Precision and recall for related-risk suggestions
- Agreement with human reviewers on defined quality issues
- Unsupported-suggestion rate
- Changed-meaning incidents

### Product Measures

- Useful-finding rate
- Acceptance and edit rate
- Rejection and defer rate
- User correction effort
- Review-agenda usefulness

### Operational Measures

- Preparation time per register
- Human-review workload
- Processing time
- Cost per reviewed register

### Business Measures

- Improvement in register completeness
- Reduction in meeting time spent cleaning entries
- Improvement in action and evidence readiness

All targets remain provisional until discovery, labelling and prototype evaluation are completed.

## 15. Responsible AI and Governance

Key controls include:

- Original and suggested text shown side by side
- Clear separation of fact, inference and recommendation
- Human confirmation before any programme-risk change
- Role-based access
- Synthetic data in the prototype
- User correction, rejection and defer controls
- Prompt, rule, model and dataset versioning
- Complete audit trail
- Manual fallback
- Launch blockers for fabricated facts, changed meaning, confidentiality failure or automatic consequential decisions

## 16. MVP-to-Revenue Direction

The proposed commercial path is:

```text
Discovery
→ Clickable Prototype
→ Controlled MVP Pilot
→ First Paid Pilot
→ Annual B2B Subscription
→ Expansion to Additional Automotive Programmes
```

The first commercial offer should be a fixed-scope paid pilot for one automotive component programme, one risk-register format and one review team. Final pricing will be determined only after buyer and willingness-to-pay interviews.

A later recurring model may use:

- Annual platform subscription
- Price per active programme
- Reviewer-seat tier
- Monthly risk-register volume
- Additional configuration, integration and support fees

## 17. Key Assumptions to Validate

- The problem occurs frequently enough to justify a product.
- Automotive programme teams will allow approved AI assistance in this workflow.
- Users will review and correct findings rather than blindly accept them.
- Synthetic and de-identified data can support early evaluation.
- The product can improve preparation without changing intended risk meaning.
- Buyer willingness to pay exists for a controlled pilot.

## 18. Current Recommendation

Proceed with discovery and a narrow clickable prototype. Do not proceed to production deployment or commercial claims until the team has completed stakeholder interviews, PRD validation, labelled evaluation data, usability testing, comparative evaluation and buyer research.

## 19. Evidence Status

The current strategy is based on the approved assignment direction and product assumptions. The following evidence is still required:

- Discovery interviews
- Current-workflow baseline
- User quotations
- Human-labelled evaluation dataset
- Prototype usability results
- Measured time reduction
- Actual processing and review cost
- Buyer willingness-to-pay evidence
- Final go, rework or stop recommendation
