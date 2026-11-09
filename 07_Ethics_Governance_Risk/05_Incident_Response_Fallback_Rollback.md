# Incident Response, Fallback and Rollback

## Incident Categories

### Severity 1: Critical

Examples:

- Confidential data exposure
- Unauthorised official register change
- Automatic approval or closure
- Systematic fabrication of programme facts

Response: stop the affected function immediately, notify authorised stakeholders, preserve evidence and begin formal incident response.

### Severity 2: High

Examples:

- Meaning-changing rewrites
- Repeated false related-risk suggestions
- Major audit-log failure
- Material provider degradation

Response: disable the affected AI feature, move to rules-only or manual workflow, investigate and retest before restoration.

### Severity 3: Moderate

Examples:

- Isolated irrelevant challenge question
- Performance or latency issue
- Incorrect evidence-age warning

Response: record, triage, correct configuration or prompt, and include in the next regression test.

## Incident Workflow

```text
Detect incident
→ Stop or isolate affected capability
→ Preserve logs and versions
→ Notify accountable owner
→ Assess scope and severity
→ Use manual or rules-only fallback
→ Correct configuration, rule, prompt or model
→ Run regression evaluation
→ Approve or reject restoration
→ Document learning and preventive change
```

## Manual Fallback

If AI is unavailable or unsafe:

1. Continue deterministic mandatory-field and date checks where available.
2. APQP Coordinator performs semantic quality review manually.
3. NPD Project Manager confirms related-risk, mitigation and agenda decisions.
4. Record the fallback mode and reviewer decisions.
5. Do not hide the absence of AI from users.

## Rollback Requirements

A production candidate should retain:

- Last approved model and prompt configuration
- Last approved deterministic rules
- Versioned evaluation set
- Release notes
- Database and register backup where applicable
- Tested instructions for disabling each AI-assisted capability

## Communications

Incident communication should state:

- What happened
- Which programme or records may be affected
- What is confirmed versus under investigation
- Immediate containment
- Required user action
- Expected next update
- Accountable contact

## Recovery Criteria

Restore a disabled capability only after:

- Root cause is understood
- Corrective change is reviewed
- Regression evaluation passes
- Meaning-preservation and unsupported-fact checks pass
- Audit logging works
- Accountable owner approves restoration

## Post-Incident Review

Record the timeline, impact, contributing factors, corrective actions, owners, dates, validation evidence and required changes to the PRD, model card, risk register and training.
