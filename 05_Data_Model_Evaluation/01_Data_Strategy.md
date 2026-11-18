# Data Strategy

## 1. Purpose

The data strategy defines how RiskReview AI will acquire, classify, prepare, govern, secure, and monitor the data required for enterprise AI risk assessment. The strategy supports automotive Artificial Intelligence and Electronic Control Unit use cases as the primary domain, wind-turbine operations as the secondary domain, and cross-enterprise governance analysis.

RiskReview AI uses data to support evidence-linked findings and human decisions. Data quality, provenance, access, representativeness, and version history must be established before model output is used in a material risk, launch, or commissioning decision.

## 2. Data Objectives

- Create a common, traceable enterprise AI risk dataset.
- Combine structured risk records with approved evidence and monitoring signals.
- Preserve source, owner, version, timestamp, and intended-use information.
- Support deterministic validation and contextual model analysis.
- Enable domain-specific evaluation for automotive and wind-energy use cases.
- Protect confidential, proprietary, personal, and supplier data.
- Support audit, incident investigation, drift monitoring, and revalidation.

## 3. Data Sources

### 3.1 Automotive AI and ECU Data

- Programme and enterprise risk registers
- ECU and ADAS validation reports
- Hardware-in-the-Loop and simulation results
- Thermal, latency, and performance test logs
- Fleet telemetry and incident records
- OTA model and software update logs
- Model Cards and Data Sheets for Datasets
- Supplier validation, change, and cybersecurity evidence
- Regional and operating-condition performance results

### 3.2 Wind-Turbine Data

- Supervisory Control and Data Acquisition signals
- Vibration, temperature, power, wind, and condition-monitoring data
- Maintenance history and inspection findings
- Predictive-maintenance alerts
- Wake-steering and control-model outputs
- Sensor calibration and drift records
- Operational incidents and downtime records
- Supplier model, hardware, and software evidence

### 3.3 Cross-Enterprise Governance Data

- Human approval and escalation records
- Risk scores and mitigation status
- Model, dataset, software, hardware, and supplier versions
- Cybersecurity and access-control logs
- Privacy and data-processing records
- Explainability reports, including TCAV and SHAP outputs where suitable
- Cost, delay, incident-probability, and loss-avoidance assumptions
- Audit findings and exception records

## 4. Data Classification

| Classification | Examples | Minimum Handling Requirement |
|---|---|---|
| Public | Published standards, public product information | Source citation and version/date record |
| Internal | Policies, generic risk templates, non-sensitive reports | Authenticated access and approved retention |
| Confidential | Validation results, programme risks, supplier evidence | Role-based access, encryption, access logging, restricted export |
| Highly Restricted | Personal data, proprietary models, security findings, vehicle or asset identifiers | Explicit approval, least privilege, encryption, controlled processing, strict retention and deletion |
| Synthetic | Artificial test records with no real organisation or person | Clear synthetic label and prohibition on production claims |

## 5. Minimum Data Model

Every material risk record should contain:

- Unique risk identifier
- Domain, use case, asset, and lifecycle stage
- Risk title and cause-event-impact statement
- Operational, financial, data/AI, cybersecurity, and continuity impacts
- Human owner and authorised reviewer
- Inherent likelihood and impact
- Proposed controls and action due dates
- Evidence references and evidence freshness date
- Model, dataset, software, hardware, and supplier versions
- Human disposition and rationale
- Residual likelihood and impact
- Monitoring indicators and revalidation triggers

## 6. Data Quality Dimensions

| Dimension | Control |
|---|---|
| Completeness | Mandatory-field validation and evidence-gap checks |
| Accuracy | Source verification and authorised human review |
| Consistency | Common taxonomy, field definitions, score range, and date format |
| Timeliness | Evidence freshness dates and overdue-action alerts |
| Validity | Schema, type, range, formula, and relationship checks |
| Uniqueness | Duplicate identifier checks and related-risk review |
| Representativeness | Coverage by region, operating condition, asset type, and relevant affected group |
| Traceability | Source, owner, version, transformation, reviewer, and timestamp history |

A material finding must not be approved when required evidence is missing, unverifiable, materially outdated, or outside the approved intended use.

## 7. Data Lifecycle

### 7.1 Acquire

Use approved connectors, file uploads, system exports, or monitored events. Record the source system, extraction date, owner, purpose, and access approval.

### 7.2 Ingest and Validate

Check schema, mandatory fields, file type, date format, value range, duplicate identifiers, formula consistency, and malicious or misleading content.

### 7.3 Prepare

Standardise terminology, preserve original text, remove unnecessary personal data, link evidence, and create versioned transformations. Derived fields must remain traceable to the source.

### 7.4 Label

Qualified reviewers label expected findings, error severity, evidence sufficiency, and final adjudication. Critical and High cases should receive independent review and documented disagreement resolution.

### 7.5 Use

Allow data use only for the approved purpose, role, domain, and model version. Separate development, validation, test, and production datasets.

### 7.6 Monitor

Track data drift, missing values, delayed feeds, sensor quality, label disagreement, access anomalies, and changes in source systems or supplier evidence.

### 7.7 Retain and Delete

Apply approved retention periods. Delete or archive records when the purpose expires, legal or contractual requirements are met, and audit obligations allow disposal.

## 8. Synthetic Data Strategy

Synthetic data will be used when real enterprise data is confidential, unavailable, sparse, or unsuitable for early development.

Synthetic records must:

- Be labelled `Synthetic`.
- Avoid real people, organisations, vehicles, turbines, sites, and incidents.
- Cover positive, negative, incomplete, ambiguous, and high-consequence cases.
- Include automotive, wind-energy, and cross-enterprise scenarios.
- Contain realistic schema and governance fields.
- Be reviewed for unrealistic shortcuts or accidental leakage.

Synthetic data may test pipelines and workflows but cannot prove production accuracy, actual risk reduction, loss avoidance, return on investment, payback, safety, or regulatory compliance.

## 9. Training, Validation, and Test Separation

- **Development data:** Used to create rules, prompts, model behaviour, and interfaces.
- **Validation data:** Used to tune thresholds and select configurations.
- **Test data:** Held back until the system and thresholds are fixed.
- **Pilot data:** Collected under approved access, security, and human-review controls.

Records should not appear in more than one split through duplication, paraphrasing, or shared incident evidence. Split decisions and dataset versions must be recorded.

## 10. Data Governance Roles

| Role | Responsibility |
|---|---|
| Data Owner | Approves purpose, access, retention, and sharing |
| Data Steward | Maintains definitions, quality, lineage, and issue resolution |
| Domain Expert | Confirms technical meaning and evidence relevance |
| Privacy and Security Reviewer | Approves personal, confidential, and security-sensitive processing |
| Model Owner | Records intended use, dataset version, limitations, and monitoring |
| Human Labeller | Creates and explains reference labels |
| Governance Decision Authority | Approves material use, exceptions, and residual risks |
| Audit Reviewer | Verifies traceability, access history, decisions, and control operation |

## 11. Privacy, Security, and Supplier Controls

- Apply data minimisation and purpose limitation.
- Use role-based access and least privilege.
- Encrypt confidential data in transit and at rest.
- Do not send proprietary or personal data to unapproved model services.
- Treat uploaded evidence as untrusted input and protect against prompt injection and malicious files.
- Require suppliers to provide data provenance, model documentation, validation evidence, change notification, incident notification, audit rights, and deletion or return terms.
- Record cross-border processing, retention, and access restrictions where applicable.

## 12. Monitoring Indicators

- Missing-field and invalid-record rate
- Evidence freshness and unresolved evidence gaps
- Data drift and schema change
- Sensor calibration and feed availability
- Label disagreement and adjudication rate
- Domain and operating-condition coverage
- Access anomalies and unauthorised export attempts
- Supplier evidence completeness
- Records requiring revalidation after model, data, software, hardware, supplier, or regulatory change

## 13. Data Readiness Gates

| Gate | Requirement |
|---|---|
| Development Ready | Approved synthetic or anonymised schema, source record, and quality checks |
| Evaluation Ready | Versioned dataset, documented labels, separate test set, and coverage review |
| Pilot Ready | Approved access, security, privacy, retention, representative evidence, and human reviewers |
| Deployment Ready | Stable data pipeline, monitoring, lineage, incident response, rollback, and revalidation process |

A use case cannot progress when required data ownership, provenance, access approval, representativeness, or monitoring is missing.
