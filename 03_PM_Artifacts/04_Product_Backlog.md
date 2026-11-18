# Product Backlog

## 1. Backlog Conventions

Priority uses P0 (mandatory), P1 (high), P2 (medium), and P3 (later). Story points are relative estimates for planning, not elapsed days. Status is initially **Proposed** until the team confirms delivery evidence.

## 2. Prioritised Backlog

| ID | Backlog item | Priority | Story points | Dependency | Definition of Done summary | Status |
|---|---|---:|---:|---|---|---|
| PB-01 | Define common risk data model | P0 | 5 | None | Fields, types, validation and examples documented | Proposed |
| PB-02 | Build workbook/file import validation | P0 | 8 | PB-01 | Valid records imported; errors identified by row/field | Proposed |
| PB-03 | Implement inherent/residual formulas | P0 | 3 | PB-01 | Calculations tested for boundaries 1–25 | Proposed |
| PB-04 | Implement heatmap and tier mapping | P0 | 5 | PB-03 | Low/Medium/High/Critical mapping tested | Proposed |
| PB-05 | Create evidence-gap rules | P0 | 5 | PB-01 | Missing/stale cases detected in labelled tests | Proposed |
| PB-06 | Develop related-risk suggestion prototype | P0 | 8 | PB-01 | Candidate link and rationale shown; no auto-merge | Proposed |
| PB-07 | Build explanation and limitations panel | P0 | 5 | PB-06 | Evidence, version, uncertainty and limits displayed | Proposed |
| PB-08 | Implement human disposition workflow | P0 | 8 | PB-07 | Accept/reject/modify/escalate stored with justification | Proposed |
| PB-09 | Implement audit history | P0 | 8 | PB-02, PB-08 | Inputs, outputs, versions and decisions traceable | Proposed |
| PB-10 | Enforce Critical gate blocking | P0 | 5 | PB-04, PB-08 | Unresolved Critical item prevents progression | Proposed |
| PB-11 | Define role and permission model | P0 | 5 | None | Reviewer permissions and segregation documented/tested | Proposed |
| PB-12 | Prepare labelled automotive test cases | P0 | 8 | PB-01 | Expected results and reviewer labels approved | Proposed |
| PB-13 | Prepare labelled wind-energy test cases | P1 | 8 | PB-01 | Expected results and reviewer labels approved | Proposed |
| PB-14 | Implement basic drift alert | P1 | 8 | Monitoring data | Metric, threshold and investigation workflow tested | Proposed |
| PB-15 | Build supplier evidence checklist | P1 | 5 | Supplier requirements | Gap, owner, due date and blocker status recorded | Proposed |
| PB-16 | Create role-based dashboard | P1 | 8 | PB-11 | Permitted risks, actions and gate status visible | Proposed |
| PB-17 | Export governance report | P1 | 5 | PB-09 | Export preserves traceability | Proposed |
| PB-18 | Run shadow-mode comparison | P1 | 13 | PB-12, PB-13 | AI and expert outputs compared and errors classified | Proposed |
| PB-19 | Complete privacy and security review | P0 | 8 | Architecture | Risks, controls and approval recorded | Proposed |
| PB-20 | Test rollback and restricted operation | P1 | 8 | Deployment design | Trigger, authority and outcome documented | Proposed |
| PB-21 | Measure baseline and pilot value | P1 | 5 | Discovery access | Time, quality and adoption compared | Proposed |
| PB-22 | Record AI usage and human verification | P0 | 3 | All artifacts | Prompt, output, edits and approver recorded | Proposed |
| PB-23 | Create portfolio analytics | P2 | 13 | Multiple pilots | Cross-programme trends validated | Proposed |
| PB-24 | Add synthetic edge-case generation | P2 | 13 | Domain validation | Generated cases reviewed and limitations recorded | Proposed |
| PB-25 | Supplier benchmarking | P3 | 13 | Comparable data | Transparent methodology and data rights approved | Proposed |

## 3. Initial Sprint Proposal

### Sprint 1

PB-01, PB-03, PB-11 and PB-12.

### Sprint 2

PB-02, PB-04, PB-05 and PB-19.

### Sprint 3

PB-06, PB-07, PB-08 and PB-09.

### Sprint 4

PB-10, PB-15, PB-17 and PB-22.

Sprint duration and capacity must be set by the team. No calendar commitment is implied by this proposal.

## 4. Definition of Ready

A backlog item is ready when the user, value, data, acceptance criteria, human owner, failure consequence, dependency and evaluation method are defined.

## 5. Definition of Done

An item is done when implementation, tests, security/privacy checks, documentation, human review, error evidence and version-controlled approval are complete.

## Professor-Expectation Alignment

This artifact supports the professor's expected evidence of product-management discipline, expanded enterprise scope, appropriate AI use, human oversight, Responsible AI, Explainable AI, measurable evaluation, commercial relevance, and critical reflection. Any score, target, or forecast without observed pilot evidence is labelled as an assumption or proposed target.
