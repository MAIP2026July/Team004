# Synthetic Data Specification

## Purpose

The synthetic dataset supports controlled development and evaluation of the RiskReview AI model without using confidential automotive, supplier, vehicle, turbine, employee, or customer data.

## Dataset

`Synthetic_Risk_Register.csv` contains 15 synthetic enterprise AI risk records:

- Seven automotive records
- Four wind-energy records
- Four cross-enterprise governance records

The records cover model performance, Electronic Control Unit deployment, cybersecurity, supplier governance, Responsible AI, privacy, platform dependency, predictive maintenance, sensor quality, wake steering, explainability, monitoring, human approval, and commercial assumptions.

## Schema

| Field | Type | Description |
|---|---|---|
| `Risk_ID` | Text | Unique synthetic record identifier |
| `Domain` | Category | Automotive, Wind Energy, or Cross-Enterprise |
| `Risk_Category` | Category | Risk classification |
| `Risk_Title` | Text | Short risk statement |
| `Cause` | Text | Condition that may create the risk |
| `Uncertain_Event` | Text | Event that may occur |
| `Impact` | Text | Enterprise consequence |
| `Human_Owner` | Text | Accountable role, not a real person |
| `Inherent_Likelihood` | Integer 1–5 | Human-labelled baseline likelihood |
| `Inherent_Impact` | Integer 1–5 | Human-labelled baseline impact |
| `Inherent_Score` | Integer 1–25 | Likelihood multiplied by impact |
| `Data_Origin` | Category | Synthetic for every current row |
| `Status` | Category | Workflow status |
| `Evidence_Reference` | Text | Illustrative supporting evidence |
| `Expected_Model_Finding` | Text | Expected model observation or challenge |
| `Human_Label` | Category | Human adjudication status |

## Generation Rules

- No row represents an actual company, vehicle, supplier, turbine, site, incident, or individual.
- Each record contains a cause, uncertain event, and impact.
- Likelihood and impact use the approved 1–5 scale.
- Scores are arithmetic results, not measured enterprise exposure.
- Owners are functional roles, not personal names.
- Evidence references describe the type of evidence required, not real attachments.
- Cost and ROI examples remain scenario assumptions unless supported by evidence.

## Data Quality Checks

- `Risk_ID` must be unique.
- Likelihood and impact must be integers from 1 to 5.
- Inherent score must equal likelihood × impact.
- Required text fields must not be blank.
- `Data_Origin` must remain `Synthetic` for this dataset.
- A material finding cannot be marked approved without a human label.

## Intended Use

The dataset may be used for:

- File ingestion and schema validation
- Cause-event-impact review
- Evidence-gap detection
- Related-risk suggestion testing
- Risk-tier calculation
- Human labelling and disagreement analysis
- Evaluation-pipeline testing

## Prohibited Use

The dataset must not be used to claim production performance, actual risk reduction, regulatory compliance, loss avoidance, return on investment, or safety certification.
