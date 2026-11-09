# Synthetic Dataset Specification

## Purpose
Provide a safe, reproducible automotive programme-risk dataset for prototype development and offline evaluation.

## Required columns
`risk_id`, `programme_name`, `apqp_phase`, `workstream`, `risk_category`, `cause`, `event`, `impact`, `risk_statement`, `risk_owner`, `mitigation`, `action_owner`, `due_date`, `review_date`, `evidence_reference`, `evidence_date`, `status`.

## Evaluation labels
- completeness_issue
- cause_event_impact_quality
- mitigation_alignment
- evidence_freshness
- related_risk_group
- meaning_preserved
- reviewer_notes

## Coverage
Include requirements, design, prototypes, tooling, suppliers, raw material, validation, manufacturing engineering, MSA, process capability, PFMEA action closure, Control Plan, PPAP, capacity, packaging, logistics, trial build and Start of Production.

## Challenge cases
Include similar wording with different root causes, different wording with the same root cause, valid short risks, non-native English writing, acronyms, missing dates and mitigations that are monitoring activities rather than preventive controls.
