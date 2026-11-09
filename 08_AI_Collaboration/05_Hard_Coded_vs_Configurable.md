# Hard-Coded Versus Configurable Elements

## Purpose

The prototype may use hard-coded demonstration values. A production product should expose appropriate customer-specific settings through controlled configuration rather than source-code changes.

## Classification

| Element | Prototype Treatment | Production Treatment | Approval Required |
|---|---|---|---|
| Programme name | Hard-coded fictional value | Configurable per programme | APQP Coordinator |
| Risk categories | Hard-coded sample taxonomy | Customer-configurable controlled list | Programme governance |
| APQP stages | Hard-coded sample stages | Configurable milestone model | NPD Project Manager |
| Mandatory fields | Hard-coded rules | Configurable template policy | Programme governance |
| Evidence-age threshold | Hard-coded provisional value | Configurable by category | Risk governance owner |
| Similarity threshold | Hard-coded provisional value | Validated and version-controlled | Product owner and model reviewer |
| User roles | Hard-coded demo users | Role-based access configuration | Customer administrator |
| Escalation route | Simulated | Configurable workflow | Programme governance |
| AI model | Fixed demonstration choice | Approved provider/model configuration | Security and product owner |
| Prompt | Fixed prototype prompt | Version-controlled approved prompt | Product owner |
| Audit fields | Fixed sample | Configurable within mandatory minimum | Compliance owner |
| Dashboard measures | Synthetic values | Derived from operational data | Product owner |
| Retention period | Not implemented | Policy-controlled configuration | Data owner |

## Items That Must Not Become Configurable Autonomous Decisions

The product must not provide a setting that enables automatic:

- Risk probability or impact assignment
- FMEA severity, occurrence, or detection rating
- PPAP approval
- Start-of-Production approval
- Risk acceptance, escalation, merger, closure, or deletion

These remain authorised human decisions.
