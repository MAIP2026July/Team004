# Incident Response, Fallback, and Rollback

## 1. Incident Categories

- Model performance or drift incident
- Data quality, provenance, privacy, or access incident
- Cybersecurity, adversarial, or OTA integrity incident
- Supplier model, software, hardware, or evidence incident
- Explainability or human-decision failure
- Automotive operational or fleet incident
- Wind-turbine maintenance, sensor, control, or continuity incident
- Unsupported financial or governance claim influencing a decision

## 2. Severity Levels

| Severity | Description | Initial Response Target |
|---|---|---|
| Sev 1 | Immediate safety, critical operational, major cyber, fleet, or multi-asset exposure | Immediate containment and executive escalation |
| Sev 2 | High impact with limited current scope or credible expansion path | Contain and begin investigation within hours |
| Sev 3 | Medium impact, no immediate critical exposure | Investigate within one business day |
| Sev 4 | Low impact or documentation issue | Correct through normal backlog and monitoring |

Exact service levels require organisational approval before deployment.

## 3. Response Workflow

1. Detect and log the incident.
2. Record affected use case, asset, model, dataset, software, hardware, and supplier versions.
3. Classify severity and assign incident commander.
4. Contain exposure through access suspension, restricted operation, model disablement, or release hold.
5. Activate fallback or rollback where defined.
6. Preserve evidence and audit records.
7. Assess safety, operational, privacy, cybersecurity, supplier, financial, and regulatory impact.
8. Notify required internal and external parties.
9. Correct the cause and validate the control.
10. Obtain human reapproval before resuming normal operation.
11. Complete lessons learned and update risks, tests, and controls.

## 4. Fallback Controls

### Automotive

- Deterministic monitor or safety wrapper
- Driver or operator alert within the approved design
- Restricted operating mode
- Disable affected AI function while preserving safe vehicle operation
- Hold OTA rollout or revert to approved software/model package
- Manual engineering and fleet review

### Wind Energy

- Revert to validated baseline control strategy
- Restrict wake-steering or optimisation mode
- Continue manual or threshold-based monitoring
- Inspect or recalibrate the affected sensor
- Isolate an affected turbine or subsystem where authorised
- Use approved maintenance decision procedures

Fallback behaviour must be tested before deployment and must not be invented during an incident.

## 5. Rollback Requirements

- Approved previous model, software, configuration, and data interface
- Integrity and compatibility verification
- Named rollback authority
- Defined trigger and maximum rollback time
- Data and decision-history preservation
- Post-rollback validation
- Communication to affected users and governance authorities

## 6. Kill-Switch and Stop Authority

The designated incident commander, cybersecurity authority, product owner, safety/quality authority, operations authority, or executive risk authority may stop or restrict operation according to the approved RACI and severity plan. The AI model has no authority to resume operation autonomously.

## 7. Incident Evidence

Capture detection source, timeline, affected scope, versions, decisions, communications, fallback or rollback action, data impact, root cause, corrective action, residual risk, and reapproval.

## 8. Testing

Run tabletop and technical exercises for:

- Compromised OTA package
- Severe model drift
- Incorrect high-confidence recommendation
- Unavailable model service
- Missing supplier evidence after a change
- Vehicle or turbine sensor corruption
- Privacy or access breach
- Rollback failure

Critical exercises should be repeated before each major scale gate and after material architecture changes.
