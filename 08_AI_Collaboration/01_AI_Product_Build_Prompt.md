# AI Product Build Prompt

## Purpose

This prompt is provided to an AI system together with the RiskReview AI Product Management artifacts. The requested output is a clickable browser prototype, not a production deployment.

## Prompt

> Using the attached Product Management artifacts, build a clickable browser prototype of **RiskReview AI**.
>
> RiskReview AI is designed for Tier 1 and Tier 2 automotive component manufacturers conducting New Product Development and New Product Introduction programmes from APQP to Start of Production.
>
> The first workflow is the monthly programme-risk and launch-readiness review. The primary users are the NPD Project Manager and APQP Coordinator.
>
> The prototype must include:
>
> 1. Automotive programme context and risk-register upload
> 2. Mandatory-field, invalid-date, overdue-action, and stale-evidence checks
> 3. Cause-event-impact structure review
> 4. Potentially related-risk comparison with a written reason
> 5. Mitigation challenge questions
> 6. Original text, supporting evidence, uncertainty, and suggested revision
> 7. Human actions: accept, edit, reject, link, merge, defer, or escalate
> 8. Verified programme review agenda
> 9. Audit record containing reviewer, reason, timestamp, rule/model/prompt version, original text, and final text
> 10. Clear labels for synthetic data, simulated AI output, and provisional thresholds
>
> Do not:
>
> - Assign project-risk probability or impact automatically
> - Replace DFMEA or PFMEA
> - Assign FMEA severity, occurrence, or detection ratings
> - Approve PPAP
> - Approve Start of Production
> - Automatically accept, merge, escalate, close, or delete risks
> - Present generated project facts as confirmed evidence
> - Use real confidential customer, supplier, drawing, or programme data
>
> After building the prototype, perform a critical self-evaluation covering:
>
> 1. Feedback on the PM artifacts
> 2. Ambiguous or missing requirements
> 3. Recommended changes
> 4. Hard-coded prototype elements
> 5. Elements that should be configurable in production
> 6. Technical, ethical, operational, and commercial risks
> 7. Evidence still required before a pilot
> 8. Claims that cannot be validated from the prototype

## Expected Deliverables From the AI

- Clickable HTML prototype
- Source files required to run locally
- Synthetic sample data only
- Prototype README and demo instructions
- Screenshots of the principal workflow
- Self-evaluation report
- List of assumptions and limitations

## Human Review Requirement

The team will review all generated code, text, sample data, thresholds, and claims. AI-generated content will not be treated as approved product evidence without human verification.
