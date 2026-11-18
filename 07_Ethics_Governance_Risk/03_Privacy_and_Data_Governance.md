# Privacy and Data Governance

## 1. Purpose

This document defines privacy and data-governance controls for automotive AI and ECU, wind-turbine, supplier, and cross-enterprise risk information processed by RiskReview AI.

## 2. Data Principles

- Purpose limitation
- Data minimisation
- Lawful and authorised processing
- Accuracy and evidence traceability
- Role-based access and least privilege
- Storage limitation and controlled deletion
- Security, confidentiality, and integrity
- Human accountability and auditability

## 3. Data Categories

| Category | Examples | Treatment |
|---|---|---|
| Risk and governance data | Risk statements, scores, controls, decisions | Role-based access and version history |
| Model and dataset data | Model Cards, Data Sheets, validation results, drift reports | Confidential access and provenance |
| Automotive data | Vehicle telemetry, ECU logs, OTA records, incident information | Data minimisation, purpose control, asset or personal-data review |
| Wind-energy data | SCADA, sensor, maintenance, asset, and operating data | Site and asset confidentiality, integrity and access control |
| Supplier data | Proprietary model, hardware, validation, and incident evidence | Contractual rights, confidentiality, audit and change controls |
| Personal data | User identity, driver or operator data, approval records | Lawful basis, minimum collection, retention, access and deletion controls |
| Synthetic data | Artificial test records | Clear synthetic label and prohibited production claims |

## 4. Data Lifecycle Controls

### Collection

Record source, owner, purpose, approval, date, domain, and sensitivity. Do not collect data merely because it may be useful later.

### Ingestion

Validate format, schema, provenance, malware, prompt-injection content, and access authority. Preserve the original record.

### Processing

Use only approved models, environments, and purposes. Derived fields and transformed evidence must remain traceable.

### Sharing

Apply contractual, geographic, confidentiality, and access restrictions. Do not upload confidential or personal data to unapproved external model services.

### Retention and Deletion

Set retention by purpose, contract, legal requirement, incident need, and audit obligation. Record deletion, return, or archival decisions.

## 5. Access Model

| Role | Typical Access |
|---|---|
| Risk Owner | Own records, actions, and approved evidence |
| Domain Reviewer | Relevant risk and technical evidence |
| Governance Authority | Material risks, exceptions, approvals, and summaries |
| Privacy or Security Reviewer | Data inventory, access, incident, and control evidence |
| Supplier Reviewer | Approved supplier evidence and contractual obligations |
| Audit Reviewer | Read-only traceability and control records |
| System Administrator | Technical administration without unnecessary content access |

Critical approvals, privileged access, and data export should use segregation of duties and enhanced logging.

## 6. Supplier Data Governance

Contracts should define:

- Data and model ownership
- Training and validation provenance
- Approved processing locations
- Subprocessors and cross-border processing
- Security and access controls
- Model, data, hardware, and software change notification
- Incident notification
- Audit and evidence rights
- Retention, deletion, return, portability, and exit support

## 7. Privacy and Data Risk Checks

Before a pilot or deployment, verify:

- The intended purpose and prohibited uses
- Whether personal or sensitive data is present
- Necessity and proportionality of each field
- Regional and cross-border restrictions
- Data-subject or affected-user communication where applicable
- Access, retention, deletion, and incident processes
- Model training and inference provider terms
- Synthetic, anonymised, pseudonymised, and real-data boundaries

## 8. Monitoring

Monitor unauthorised access, export, retention breach, missing consent or lawful basis where applicable, unapproved model use, supplier change, data drift, schema change, and evidence-provenance failure.

## 9. Incident Response

A privacy or data incident is handled through containment, access suspension, evidence preservation, impact assessment, notification assessment, remediation, and documented reapproval before processing resumes.
