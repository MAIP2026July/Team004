# Product Risk Register

## 1. Risk Method

The product risk register records enterprise AI risks across four impact dimensions:

1. Operational impact
2. Financial impact
3. Data, Responsible AI, and Explainable AI impact
4. Security and business-continuity impact

**Inherent Risk Score = Inherent Likelihood × Inherent Impact**

**Residual Risk Score = Residual Likelihood × Residual Impact**

The overall impact follows the highest applicable impact dimension. Scores are approved by authorised humans.

## 2. Risk Tiers

| Score | Tier | Required Response |
|---:|---|---|
| 17–25 | Critical | Block or restrict launch/commissioning; executive review required |
| 10–16 | High | Mandatory mitigation, senior approval, dedicated validation, and monitoring |
| 5–9 | Medium | Standard governance gate and periodic review |
| 1–4 | Low | Authorised acceptance and routine monitoring |

## 3. Core Product Risks

| ID | Domain | Risk | Inherent Score | Key Controls | Residual Target | Owner |
|---|---|---|---:|---|---:|---|
| PR-01 | Automotive | Edge-case perception failure in unfamiliar weather or road conditions | 25 | Scenario mining, representative validation, sensor fusion, deterministic monitor, ODD restriction | ≤ 9 | ADAS Engineering |
| PR-02 | Automotive | ECU latency or accuracy drift after quantisation and thermal load | 20 | Thermal bench tests, latency thresholds, fallback mode, hardware review | ≤ 9 | ECU Engineering |
| PR-03 | Automotive | OTA model or software update compromise | 20 | Signed packages, segregation of duties, staged release, monitoring, rollback | ≤ 8 | Cybersecurity and OTA Release |
| PR-04 | Automotive | Supplier black-box model without adequate evidence | 16 | Glass-Box evidence requirements, audit rights, change notification, exit plan | ≤ 9 | Supplier Quality |
| PR-05 | Automotive | Regional or demographic performance disparity | 15 | Segmented evaluation, data-coverage review, threshold and release controls | ≤ 9 | Data Governance |
| PR-06 | Automotive | Vehicle telemetry privacy and data-sovereignty exposure | 12 | Data minimisation, consent or lawful basis, retention, access, regional processing | ≤ 6 | Privacy Office |
| PR-07 | Automotive | AI hardware and platform dependency | 12 | Alternate-platform assessment, portability, inventory, dual-source and exit plan | ≤ 8 | Product and Procurement |
| PR-08 | Wind Energy | Opaque predictive-maintenance recommendation | 12 | Sensor provenance, model version, uncertainty, maintenance evidence, human review | ≤ 6 | Reliability Engineering |
| PR-09 | Wind Energy | Sensor drift produces false maintenance or control recommendations | 12 | Calibration monitoring, drift alerts, redundancy, revalidation | ≤ 6 | Operations |
| PR-10 | Wind Energy | Wake-steering model used outside validated conditions | 15 | Operating envelope, control limits, shadow mode, rollback, human approval | ≤ 8 | Control Engineering |
| PR-11 | Cross-Enterprise | Material AI decision lacks named human approver | 20 | Role-based workflow, segregation of duties, blocked gate, audit log | ≤ 4 | Enterprise Risk |
| PR-12 | Cross-Enterprise | Explainability output is treated as proof of causality | 12 | Limitation statements, reviewer training, multiple evidence types, expert review | ≤ 6 | Model Risk |
| PR-13 | Cross-Enterprise | Drift alert lacks owner, due date, or escalation | 16 | Monitoring ownership, service levels, escalation, incident workflow | ≤ 6 | MLOps |
| PR-14 | Commercial | Loss-avoidance, ROI, or payback projection lacks evidence | 12 | Assumption log, sensitivity analysis, finance review, pilot measurement | ≤ 4 | Finance and Product |

## 4. Required Risk Record Fields

- Risk ID, domain, source, title, and cause-event-impact statement
- Operational, financial, data/AI, security, and continuity impacts
- Owner and governance approver
- Inherent likelihood, impact, score, and rationale
- Controls, action owner, due date, and evidence
- Residual likelihood, impact, score, and rationale
- Status, review date, escalation, exception, and monitoring indicator
- Model, dataset, software, hardware, and supplier versions

## 5. Review Frequency

- Critical: continuous tracking and at least weekly governance review until reduced or accepted by the designated authority
- High: at least monthly review and before every relevant launch or commissioning gate
- Medium: quarterly or at the relevant product gate
- Low: periodic monitoring or when a material change occurs

## 6. Evidence Position

Current scores and targets are academic scenario values unless supported by documented organisational evidence. A lower residual score does not automatically close a risk. Closure requires control evidence, authorised approval, and continuing monitoring where applicable.
