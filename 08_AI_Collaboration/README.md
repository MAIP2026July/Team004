# 08_AI_Collaboration

## Purpose
This folder records how Artificial Intelligence was used to support the design and documentation of **RiskReview AI: Enterprise AI Risk Governance and Assurance Platform**. It makes AI contribution, self-checking, ambiguity handling, configuration boundaries, and final human accountability visible.

AI-generated content in this folder is a reviewed project artifact, not evidence that the product has passed independent assurance or regulatory certification.

## Folder Contents
| File | Purpose |
|---|---|
| `01_AI_Product_Build_Prompt.md` | Master product-building prompt, output format, and guardrails. |
| `02_AI_Self_Evaluation.md` | Quality rubric for checking AI outputs before use. |
| `03_AI_Collaboration_Log.md` | Register of material AI contributions and human modifications. |
| `04_Ambiguities_and_Change_Log.md` | Open questions, working assumptions, scope evolution, and controlled changes. |
| `05_Hard_Coded_vs_Configurable.md` | Separation between immutable safeguards, controlled policy, preferences, and model outputs. |
| `06_Human_Review_and_Final_Decisions.md` | Human decision rights, review levels, override controls, and final decision record. |

## Scope
The folder follows the expanded platform scope:
- Automotive ECUs and AI-enabled vehicle functions
- ADAS and automated-driving risk
- Connected vehicles and OTA updates
- Cybersecurity and supplier AI governance
- Responsible AI and Explainable AI
- Enterprise risk scoring, monitoring, governance gates, and auditability
- Wind-turbine monitoring as a secondary configurable application

## Collaboration Boundary
### AI may
- Draft and restructure content
- Identify possible gaps, conflicts, and relationships
- Suggest requirements, mitigations, evaluation criteria, and explanations
- Calculate deterministic values from approved inputs
- Generate alternatives for human comparison

### AI may not
- Invent evidence or authoritative scores
- Determine legal or regulatory compliance
- Accept suppliers or close material risks
- Approve safety-critical releases or production deployment
- Make final commercial, investment, or governance decisions

## Use Sequence
1. Use the build prompt to generate or revise a product artifact.
2. Apply the self-evaluation rubric.
3. Record material AI contribution in the collaboration log.
4. Capture unresolved assumptions and approved changes.
5. Confirm whether each behaviour is hard-coded, configurable, or model-derived.
6. Complete human review and preserve the final decision record.

## Submission Checks
- The collaboration log describes actual use and is not presented as a fictional activity record.
- Open ambiguities have owners or are explicitly deferred.
- Configurable thresholds are not represented as universal requirements.
- AI-generated recommendations remain distinguishable from human-approved decisions.
- No unsupported claims of certification, compliance, deployment, accuracy, ROI, or customer adoption are included.
- Dates, commit references, model versions, and final approvals are added when available.
