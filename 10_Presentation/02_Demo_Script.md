# Demonstration Script

## Demo Objective

Demonstrate how RiskReview AI processes an enterprise AI risk, produces an evidence-linked model finding, supports human review, applies a governance gate, and records the final decision.

## Demo Duration

Recommended duration: **6–8 minutes**.

## Demo Scenario

Use one synthetic automotive risk:

> An AI-enabled ECU perception model may misclassify an obstacle during severe rain because the validation dataset has limited regional weather coverage. The event may delay braking and create safety, recall, financial, and reputational exposure.

## Step 1: Open the Synthetic Risk Register

Show:

- Risk ID
- Domain and category
- Cause, uncertain event, and impact
- Human owner
- Inherent likelihood and impact
- Evidence references
- Expected model finding

Say:

> This record is synthetic and is used only to demonstrate the workflow. It does not represent an actual company, vehicle, supplier, or incident.

## Step 2: Run Deterministic Validation

Show the checks for:

- Required fields
- Date format
- Likelihood and impact ranges
- Score calculation
- Evidence reference
- Human owner

Say:

> Explicit checks are handled through deterministic rules. AI is not required to verify whether a field is blank or whether a score is outside the approved range.

## Step 3: Show the Model-Assisted Finding

Present a sample finding:

> Regional severe-weather coverage appears insufficient to support the stated deployment scope. Review the dataset coverage and add representative severe-rain validation scenarios before release.

Show:

- Finding type
- Rationale
- Evidence reference
- Model and prompt version
- Uncertainty or limitation
- Proposed next action

Say:

> The model provides a challenge and supporting context. The finding does not approve a score or decide whether the product can launch.

## Step 4: Human Review

Show the reviewer actions:

- Accept
- Modify
- Reject
- Request evidence
- Escalate

Choose **Modify** and record:

> Restrict the initial operating scope and require additional regional severe-rain validation before the next launch gate.

Say:

> The human-approved decision remains separate from the original model output. The reviewer records the reason for the modification.

## Step 5: Risk Score and Governance Gate

Use the illustrative values:

- Inherent likelihood: 5
- Inherent impact: 5
- Inherent score: 25, Critical

Explain:

> A Critical score blocks or restricts launch or commissioning. The score is calculated by the system, but the likelihood and impact values are approved by authorised humans.

Show that the gate requires:

- Representative validation evidence
- Responsible owner
- Approved controls
- Residual-risk assessment
- Governance approval

## Step 6: Audit Trail

Show the record of:

- Original risk
- Rule checks
- Original model finding
- Human modification
- Reviewer and approval role
- Model, dataset, prompt, or rule version
- Timestamp
- Gate result

Say:

> The audit trail allows internal audit, programme leadership, engineering, and governance reviewers to understand what the model proposed and what the human decided.

## Step 7: Monitoring and Revalidation

Show the monitoring triggers:

- Model or dataset change
- New deployment region
- ECU or hardware change
- OTA update
- Material incident
- Performance or fairness deterioration

Say:

> Approval is not permanent. A material change triggers reassessment and human reapproval.

## Step 8: Business Value Position

Say:

> The framework is expected to reduce manual review effort, repeated correction, avoidable rework, and validation delay. These benefits remain hypotheses until the pilot measures baseline and post-pilot results.

Do not present the 67% risk reduction, ₹710 crore loss avoidance, 7,000% ROI, or one-week payback as achieved outcomes.

## Closing Statement

> RiskReview AI provides machine-assisted analysis, but authorised humans retain final responsibility for risk acceptance, launch, commissioning, restriction, rollback, and closure.
