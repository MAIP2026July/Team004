# Launch Blockers and Decision Gates

## 1. Purpose

Decision gates prevent AI-enabled products or operational models from progressing when material evidence, controls, ownership, or human approval is missing.

## 2. Seven-Stage Gate Model

| Stage | Gate Objective | Minimum Evidence | Decision |
|---:|---|---|---|
| 1 | Strategy and intended use | Sponsor, use case, prohibited uses, risk appetite, accountable owner | Approve discovery or stop |
| 2 | Risk and data readiness | Risk map, data ownership, provenance, privacy, security, supplier evidence | Approve development or remediate gaps |
| 3 | Proof of Concept | Functional model or rules, synthetic test data, initial limitations | Approve prototype or stop |
| 4 | Functional Prototype | End-to-end workflow, Human-in-the-Loop actions, audit trail, initial evaluation | Approve MVP work or remediate |
| 5 | MVP and validation | Held-out evaluation, Critical-error review, security, explainability, fallback, rollback | Approve shadow mode or block |
| 6 | Shadow-Mode Pilot | Expert comparison, user behaviour, workflow value, incidents, residual risk | Approve controlled deployment or stop |
| 7 | Controlled Scale | Monitoring, support, revalidation, unit economics, independent assurance | Approve expansion, restrict, or roll back |

## 3. Mandatory Launch Blockers

Launch or commissioning is blocked or restricted when any of the following applies:

- Unresolved Critical risk score of 17–25
- Unresolved High risk with missing mandatory control or approval
- No named business owner, technical owner, or governance authority
- Missing intended use, prohibited use, or operating boundary
- Missing representative validation data or material test evidence
- Critical/High false-negative performance below the approved threshold
- Missing fallback, rollback, restricted-operation, or incident process
- Unresolved cybersecurity or OTA update-integrity finding
- Missing supplier model, dataset, validation, change, or incident evidence
- Material privacy, data-sovereignty, or access-control issue
- Explanation does not show evidence, uncertainty, and limitations for a material decision
- Model, dataset, software, hardware, or supplier version differs from the approved version
- Economic justification depends on unlabelled projections presented as achieved outcomes

## 4. Decision Options

At each gate, the authorised authority may:

- Approve progression
- Approve with conditions and monitoring
- Restrict the operating scope
- Request additional evidence or mitigation
- Defer the decision
- Reject progression
- Roll back to an earlier validated version
- Stop the use case

## 5. Gate Record

Every gate record includes:

- Use case and domain
- Current model, data, software, hardware, and supplier versions
- Inherent and residual risks
- Open Critical and High findings
- Required evidence and control status
- Human recommendation
- Decision, conditions, rationale, owner, and date
- Monitoring and revalidation triggers

## 6. Exceptions

A Critical exception requires designated executive or risk-board approval, documented necessity, bounded duration, compensating controls, monitoring, rollback conditions, and a mandatory re-review date. An exception must not be used to bypass law, regulation, safety, cybersecurity, privacy, or contractual obligations.

## 7. Revalidation Triggers

- Material model or prompt change
- Dataset shift or new deployment region
- ECU or hardware change
- New supplier or supplier model change
- OTA or software update
- Significant incident or near miss
- Fairness, performance, privacy, or security deterioration
- Wind-turbine sensor, control, weather, or operating-envelope change
- Regulatory or contractual change
