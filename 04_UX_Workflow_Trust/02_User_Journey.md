# User Journey

## Primary Journey

| Stage | User Action | Model or System Response | Human Decision |
|---|---|---|---|
| 1. Select context | Select an automotive AI/ECU or wind-turbine use case | Loads the relevant risk fields and governance controls | Confirm intended use and responsible owner |
| 2. Submit risk | Enter or import the risk, impact, control, dates, and evidence | Validates mandatory fields, formats, ranges, and evidence references | Correct invalid or incomplete information |
| 3. Receive assessment | Open the model findings | Shows the finding, rationale, evidence, uncertainty, and limitations | Decide whether the finding is relevant |
| 4. Verify evidence | Review linked model, dataset, supplier, cybersecurity, or operational evidence | Preserves version and evidence history | Accept, reject, modify, or request more evidence |
| 5. Review related risks | Compare suggested risk relationships | Shows the basis for similarity | Link, merge, or keep risks separate |
| 6. Approve risk inputs | Review likelihood and impact evidence | Calculates inherent and residual scores from approved inputs | Approve or revise the inputs |
| 7. Apply governance gate | Review the 5 × 5 tier and unresolved controls | Blocks or permits controlled progression | Approve mitigation, restriction, exception, or escalation |
| 8. Monitor | Review drift, incidents, fairness, and control trends | Raises change or threshold alerts | Continue, restrict, roll back, or revalidate |

## Automotive Example

An automotive reviewer assesses an AI-enabled ECU or Advanced Driver Assistance System risk. The model identifies limited edge-case evidence or a supplier transparency gap. The reviewer checks the source evidence, approves or revises the risk inputs, and escalates unresolved Critical or High exposure before launch or deployment.

## Wind-Turbine Example

An operations reviewer assesses a predictive-maintenance or wake-steering risk. The model highlights sensor drift, weak evidence, or model uncertainty. The reviewer decides whether to continue monitoring, inspect the asset, restrict operation, or require model revalidation.

## Failure and Recovery

- Invalid records return field-level errors for correction.
- Missing evidence prevents approval of a material model finding.
- Unauthorised users cannot approve Critical or High decisions.
- Material model, data, software, supplier, regulatory, or operating changes trigger reassessment.
- Original model output remains separate from the human-approved decision.

## Journey Measures

- Review preparation time
- Repeated correction or rework
- Findings accepted, rejected, modified, or escalated
- False-positive and false-negative findings
- Time to resolve Critical or High evidence gaps
- Audit-record completeness
- User-rated explanation usefulness

Efficiency and cost benefits are expected outcomes that require baseline and controlled-pilot measurement.
