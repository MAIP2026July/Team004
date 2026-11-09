# AI Self-Evaluation

## 1. Product Interpreted From the PM Artifacts

The artifacts describe a human-supervised assistant for pre-meeting quality review of automotive NPD/NPI programme risk registers. The product combines deterministic validation with AI-assisted semantic review. Authorised humans retain all consequential project-risk and launch decisions.

## 2. What Is Clear

- Initial industry and segment: Tier 1 and Tier 2 automotive component manufacturers
- Programme boundary: APQP to Start of Production
- Primary users: NPD Project Manager and APQP Coordinator
- First workflow: monthly programme-risk and launch-readiness review
- AI boundary: semantic review and challenge generation only
- Human accountability: every AI-assisted finding requires review
- Prohibited uses: no automatic scoring, PPAP approval, Start-of-Production approval, or FMEA replacement

## 3. Ambiguities and Missing Information

1. The final economic buyer has not been validated.
2. The standard customer risk-register schema is not yet confirmed.
3. Customer-specific APQP stages and terminology may differ.
4. Duplicate-risk similarity thresholds are provisional.
5. Evidence-age rules may vary by risk category and milestone.
6. The approved hosting environment and model provider are undecided.
7. Confidentiality, retention, and data-residency requirements require customer validation.
8. Pilot success thresholds do not yet have measured baselines.
9. Paid-pilot pricing and willingness to pay are unvalidated.
10. Integration targets such as spreadsheets, PLM, QMS, or project-management systems are not selected.

## 4. Recommended Changes

- Conduct at least five target-user interviews and document the findings.
- Measure manual review-preparation time before claiming improvement.
- Validate the PRD and PlantUML workflow with an NPD Project Manager or APQP Coordinator.
- Expand the synthetic dataset to at least 60 varied risk entries.
- Use two independent human labelers and resolve disagreements.
- Add difficult negative examples for related-risk detection.
- Keep deterministic findings visually separate from AI-assisted findings.
- Add abstention when evidence is insufficient or confidence is low.
- Record every override and reason in the audit trail.
- Validate thresholds by risk category before any controlled pilot.
- Keep pricing and ROI figures marked as assumptions until buyer research is completed.

## 5. Hard-Coded Prototype Elements

The following may be hard-coded for demonstration and must be labelled accordingly:

- Fictional automotive programme name
- Synthetic risk entries and sample evidence
- Example APQP stages
- Risk categories and work packages
- Demonstration users and roles
- Similarity and confidence values
- Evidence-age threshold
- Dashboard totals and charts
- Example audit records
- Model, rule, and prompt version labels
- Processing-time and cost figures

## 6. Production-Configurable Elements

A production product should allow authorised configuration of:

- Mandatory register fields
- Customer risk taxonomy
- APQP stages and milestone names
- Evidence-age rules by category
- Related-risk similarity threshold
- Reviewer roles and permissions
- Escalation and approval routes
- Action due-date and reminder rules
- Customer terminology and templates
- Model provider and approved model version
- Prompt and rule versions
- Notification, export, and reporting settings
- Retention and deletion periods
- Audit-report fields

## 7. Technical Limitations

The prototype cannot demonstrate production accuracy, scale, security, availability, integration reliability, model drift, or cost-to-serve. Synthetic data may not represent actual automotive programme language, edge cases, or confidentiality constraints.

## 8. Ethical and Operational Risks

- A suggestion may change the intended risk meaning.
- Distinct risks may be incorrectly presented as duplicates.
- A generated challenge may imply facts not present in evidence.
- Users may over-trust a fluent recommendation.
- Writing-style differences may affect quality flags.
- Confidential programme or supplier information may be exposed.
- External model changes may alter behaviour.
- Human review effort may make the product uneconomic.

## 9. Claims the Prototype Cannot Validate

The prototype does not prove:

- A specific accuracy level
- A measured time saving
- A reduction in programme delay or loss
- Customer willingness to pay
- Production security or regulatory compliance
- Fairness across organisations or writing styles
- Operational scalability
- Readiness for autonomous decision-making

## 10. Overall AI Assessment

The artifacts are sufficiently detailed to build a workflow prototype. They are not yet sufficient for production implementation or a real-data pilot. The strongest next evidence is target-user validation, baseline measurement, labelled evaluation data, and a controlled usability test.
