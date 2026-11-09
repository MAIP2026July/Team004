# Responsible AI for RiskReview AI

## Purpose

Responsible AI is treated as a product requirement, not a separate compliance statement. RiskReview AI must improve risk-register quality without fabricating programme facts, changing the intended meaning of a risk, or transferring consequential programme decisions to an AI system.

## Responsible-AI Principles

### 1. Human accountability

Authorised automotive programme personnel remain accountable for probability, impact, mitigation, escalation, acceptance, linking, merging and closure decisions. AI findings are advisory.

### 2. Transparency

Every finding must display:

- Original risk text
- Finding type
- Deterministic rule or AI-assisted status
- Evidence or comparison used
- Uncertainty indicator
- Suggested action
- Model, prompt or rule version

### 3. Contestability

The APQP Coordinator or NPD Project Manager must be able to accept, edit, reject, link, merge, defer or escalate a finding and record a reason.

### 4. Meaning preservation

Suggested wording must preserve the original cause, uncertain event and impact. If meaning may change, the system must abstain and request human clarification.

### 5. Fairness across writing styles

The system must not treat concise language, non-native English, department-specific terminology or grammatical weakness as evidence that the underlying programme risk is less important. Evaluation must include varied writing styles and workstreams.

### 6. Privacy and confidentiality

The classroom prototype uses fictional or synthetic automotive programme data only. Real customer drawings, supplier names, prices, contracts, quality records and launch information must not be uploaded.

### 7. Reliability and safety

Deterministic rules handle missing mandatory fields, date validation and overdue actions. AI is used only where semantic interpretation adds value. A manual or rules-only workflow must remain available.

## Prohibited Uses

RiskReview AI must not:

- Assign probability or impact automatically
- Replace DFMEA or PFMEA
- Assign FMEA severity, occurrence or detection ratings
- Approve PPAP
- Approve Start of Production
- Automatically create official programme risks from unsupported inference
- Automatically merge, accept, escalate, close or delete risks
- Be used for employee performance scoring

## Required Safeguards

- Original and suggested text shown side by side
- Human confirmation before any official register change
- Abstention when evidence is insufficient
- Role-based access in any production pilot
- Versioned rules, prompts, models and evaluation sets
- Complete audit history
- Manual fallback
- Incident reporting and rollback procedure

## Responsible-AI Evaluation

The team will measure:

- Unsupported-fact rate
- Meaning-change rate
- False related-risk suggestion rate
- Human rejection and correction rate
- Performance by workstream and writing style
- Audit-record completeness
- User understanding of AI versus rule-based findings

## Evidence Status

The controls above are design requirements. Production safety, fairness and reliability have not yet been demonstrated. Prototype outputs must be labelled synthetic, simulated or provisional as applicable.
