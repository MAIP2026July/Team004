# Ambiguities and Change Log

## 1. Purpose
This document distinguishes unclear requirements from confirmed changes. It prevents AI-generated assumptions from becoming product facts without review.

## 2. Ambiguity Handling Method
1. Record the unclear point and affected artifact.
2. State the current working assumption.
3. Identify impact if the assumption is wrong.
4. Assign an owner and target resolution point.
5. Mark the item Open, Resolved, Deferred, or Rejected.
6. Update every dependent artifact after resolution.

## 3. Ambiguity Register
| ID | Ambiguity | Working treatment | Impact | Status |
|---|---|---|---|---|
| AMB-001 | Whether wind energy is equal to the automotive scope | Automotive remains primary; wind demonstrates configurability and cross-industry extension. | Prevents an unmanageably broad MVP. | Resolved |
| AMB-002 | Whether AI may assign probability and impact | AI may suggest review questions, but authoritative values require approved data or authorised human input. | Avoids fabricated risk scores. | Resolved |
| AMB-003 | Whether risk thresholds are universal | 1-4 Low, 5-9 Moderate, 10-16 High, and 17-25 Critical are defaults stored as configuration. | Enterprises may use different risk appetite. | Resolved |
| AMB-004 | Whether XAI output proves model correctness | XAI supports interpretation only; validation, monitoring, and human review remain necessary. | Prevents false assurance. | Resolved |
| AMB-005 | Which regulations apply to each deployment | Legal and compliance applicability must be confirmed by jurisdiction, product, data, and intended use. | Incorrect claims could create compliance exposure. | Open |
| AMB-006 | Availability of production and supplier data | Use synthetic or de-identified demonstration data until authorised data is available. | Limits external validity of prototype results. | Resolved for prototype |
| AMB-007 | Exact paid-pilot pricing and ROI | Treat commercial values as hypotheses until customer discovery and cost validation. | Prevents unsupported revenue claims. | Open |
| AMB-008 | Model and hosting stack | Keep provider, model, and deployment environment configurable during prototype stage. | Avoids premature vendor lock-in. | Deferred |

## 4. Change Log
| Version | Change | Reason | Affected areas | Decision |
|---|---|---|---|---|
| v1.0 | Focused on automotive NPD/NPI risk-register review. | Initial narrow use case. | Product strategy and prototype. | Superseded |
| v2.0 | Expanded to an Enterprise AI Risk Governance and Assurance Platform. | Represent broader enterprise AI product-management and governance opportunity. | Entire repository. | Approved |
| v2.1 | Added ECU, ADAS, connected-vehicle, OTA, cybersecurity, and supplier-governance contexts. | Define concrete high-impact automotive applications. | Scope, risks, requirements, workflow. | Approved |
| v2.2 | Added wind-turbine monitoring as secondary application. | Demonstrate configurable cross-industry design. | Strategy, data model, use cases. | Approved with boundary |
| v2.3 | Embedded NIST AI RMF, RAI, XAI, and human governance gates. | Strengthen trustworthy AI lifecycle controls. | Workflow, governance, evaluation. | Approved |
| v2.4 | Retained existing numbered GitHub folder and file structure. | Prevent duplication and preserve repository continuity. | Repository documentation. | Approved |
| v2.5 | Added explicit AI collaboration and final human-decision records. | Improve transparency and reproducibility. | Folder 08 and audit approach. | Approved |

## 5. Change-Control Rule
A change affecting scope, safety, decision rights, data, risk thresholds, compliance, model behaviour, or release criteria requires an entry, impact review, owner, approval, and version update. Editorial changes may be recorded through Git history only.
