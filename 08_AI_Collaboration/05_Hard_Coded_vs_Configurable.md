# Hard-Coded vs Configurable Design

## 1. Purpose
RiskReview AI must be stable enough to control critical behaviour and flexible enough to support different enterprises, industries, jurisdictions, and risk appetites. This document separates immutable safeguards from configurable policy and presentation settings.

## 2. Design Categories
| Category | Meaning |
|---|---|
| Hard-coded safeguard | Cannot be changed through normal user configuration. A controlled software release is required. |
| Controlled configuration | Can be changed only by an authorised administrator with approval and audit logging. |
| User preference | Can be changed by an authorised user without changing governance policy. |
| Model-derived output | Generated at runtime and always subject to validation and human review. |

## 3. Hard-Coded Safeguards
- AI cannot make final safety-critical, legal, regulatory, supplier-acceptance, risk-closure, production-release, or investment decisions.
- Every material recommendation must retain evidence, model/version, timestamp, and decision history.
- Missing required evidence cannot be silently replaced with invented content.
- Failed validation and human rejection cannot be deleted from the audit trail by normal users.
- High-impact actions require authentication, role-based access, and segregation of duties.
- Inputs and outputs must be handled according to data-access classification.
- The interface must provide Accept, Modify, Reject, and Escalate controls where an AI recommendation affects governance.

## 4. Controlled Configuration
| Configurable item | Example default | Control required |
|---|---|---|
| Risk bands | Low 1-4; Moderate 5-9; High 10-16; Critical 17-25 | Risk-policy owner approval |
| Probability and impact scales | 1 to 5 | Governance administrator approval |
| Mandatory evidence fields | Owner, action, due date, evidence reference | Workflow-owner approval |
| Escalation matrix | High to domain lead; Critical to executive gate | Role and policy approval |
| Confidence threshold | Route below configured value to review | Model-risk approval and testing |
| Review cadence | Continuous, weekly, monthly, or gate-based | Process-owner approval |
| Industry taxonomy | Automotive or wind-energy terms | Domain administrator approval |
| RAI checks | Fairness, privacy, safety, security, transparency | RAI owner approval |
| Model/provider | Approved model and version | Architecture, security, and model-risk approval |
| Retention period | Based on policy and legal requirements | Data owner and legal approval |
| Notification rules | Role, severity, due-date triggers | Workflow administrator approval |

## 5. User Preferences
Users may configure language, dashboard filters, saved views, notification channel, and report layout within access rights. User preferences cannot weaken required review, evidence, security, or audit controls.

## 6. Model-Derived Outputs
Risk relationships, summaries, evidence-gap suggestions, mitigation proposals, confidence values, explanations, and prioritisation recommendations are runtime outputs. These are neither hard-coded facts nor approved policy. The system must label these outputs, cite inputs, and preserve human decision options.

## 7. Configuration Record
Each controlled change should capture:
```text
configuration_key
previous_value
new_value
business_reason
requested_by
approved_by
approval_date
validation_result
effective_date
rollback_version
```

## 8. Example
An enterprise changes the Critical band from 17-25 to 20-25. The platform does not allow an ordinary reviewer to make that change. A risk-policy owner approves the configuration, test cases confirm reclassification behaviour, the effective date is recorded, and existing reports retain the policy version used at the time.

## 9. Failure Modes and Controls
- **Excessive hard-coding:** creates costly deployments and code forks. Use versioned configuration for policy differences.
- **Excessive configurability:** permits inconsistent or unsafe governance. Keep decision authority and evidence integrity immutable.
- **Unreviewed configuration drift:** produces different outcomes across teams. Use approval, validation, versioning, and periodic comparison.
- **Vendor lock-in:** limits model replacement. Isolate provider-specific interfaces and maintain evaluation baselines.
