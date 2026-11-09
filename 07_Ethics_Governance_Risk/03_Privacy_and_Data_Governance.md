# Privacy and Data Governance

## Data Boundary

The classroom prototype will use only fictional or synthetic automotive programme-risk data. No real customer, supplier, employee, drawing, contract, quality, commercial or launch data may be committed to GitHub.

## Data Minimisation

Collect only fields required for the workflow, such as:

- Risk ID
- Programme stage
- Workstream
- Cause, uncertain event and impact
- Owner and action owner
- Mitigation, contingency and trigger
- Due date, review date and last-updated date
- Evidence reference
- Human decision and rationale

Avoid direct personal identifiers. Use role names or fictional user names in the prototype.

## Purpose Limitation

Data is used only to:

- Validate risk-register completeness
- Support semantic quality review
- Compare potentially related risks
- Challenge mitigation quality
- Prepare a human-verified review agenda
- Evaluate the prototype

The data must not be reused for employee scoring, supplier blacklisting, autonomous approval or unrelated model training.

## Access Control

A production pilot should use role-based access:

- Risk Owner: create and update assigned risks
- APQP Coordinator: review findings and prepare agenda
- NPD Project Manager: confirm consequential decisions
- Specialist: review escalated technical questions
- Auditor or Administrator: view authorised audit records

Least privilege and separation of duties should apply.

## Retention and Deletion

Prototype synthetic data may remain in the academic repository. Any future pilot must define customer-approved retention periods for:

- Uploaded register versions
- AI findings
- Human decisions
- Audit logs
- Evaluation samples
- Incident records

Deletion must remove data from active storage and follow the provider's approved backup-retention process. Final periods are TBD after customer and legal review.

## Security Requirements for a Future Pilot

- Encryption in transit and at rest
- Customer-approved hosting region
- Authentication and role-based authorisation
- Environment separation
- Secret management
- Audit logging
- Dependency and vulnerability review
- Backup and recovery testing
- Provider data-training opt-out or equivalent contractual control

## Data Quality and Lineage

Each evaluation record should retain:

- Dataset version
- Source classification: synthetic, transformed or approved pilot data
- Label version
- Reviewer identity or reviewer code
- Disagreement resolution
- Model, prompt and rule version
- Evaluation date

## GitHub Rules

Do not commit:

- Real automotive programme files
- Customer or supplier names
- Credentials or API keys
- Proprietary drawings or specifications
- Contracts, prices or personally identifiable information

Use `.gitignore`, secret scanning and manual review before each commit.

## Data-Governance Decision Gate

A real-data pilot cannot begin until the customer approves data categories, access, retention, hosting, incident response and model-provider terms.
