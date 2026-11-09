# AI and Rules Architecture

## Hybrid design

### Deterministic rules
- Mandatory-field checks
- Invalid date checks
- Overdue action checks
- Missing owner checks
- Evidence-age calculation

### AI-assisted functions
- Cause-event-impact review
- Related-risk candidate retrieval and ranking
- Mitigation challenge questions
- Controlled meeting-agenda drafting

### Human decisions
- Confirm official risk wording
- Set probability and impact
- Accept, edit, reject, link, merge or defer a finding
- Approve mitigation, escalation, closure, PPAP and Start of Production

## Processing flow
1. Ingest the approved risk-register schema.
2. Run deterministic validation.
3. Create AI-assisted findings with evidence and uncertainty.
4. Present original text beside the finding.
5. Require human action and rationale.
6. Record rule, prompt/model version, reviewer and timestamp.

## Fallback
If AI is unavailable, deterministic checks continue and reviewers use the normal manual review process.
