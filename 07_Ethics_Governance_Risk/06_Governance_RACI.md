# Governance RACI

## 1. RACI Definitions

- **R – Responsible:** Performs the work
- **A – Accountable:** Owns the final decision
- **C – Consulted:** Provides specialist input
- **I – Informed:** Receives status or decision information

## 2. Roles

- Executive Risk Board (ERB)
- Product or Programme Leader (PPL)
- AI/Model Owner (AMO)
- Domain Engineering (DE)
- Safety and Quality (SQ)
- Cybersecurity (CS)
- Data Governance and Privacy (DGP)
- Operations and Maintenance (OM)
- Procurement and Supplier Quality (PSQ)
- MLOps and Platform (MP)
- Internal Audit and Compliance (IAC)

## 3. Governance RACI Matrix

| Activity | ERB | PPL | AMO | DE | SQ | CS | DGP | OM | PSQ | MP | IAC |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Approve intended and prohibited use | A | R | C | C | C | C | C | C | C | I | C |
| Approve risk appetite and Critical exception | A | R | C | C | C | C | C | C | C | I | C |
| Create and maintain risk record | I | A | R | R | C | C | C | C | C | I | I |
| Approve likelihood and impact inputs | I | A | C | R | C | C | C | C | C | I | I |
| Prepare data and model evidence | I | C | A/R | R | C | C | C | C | C | R | I |
| Approve privacy and data use | I | C | C | I | I | C | A/R | I | C | C | I |
| Approve cybersecurity and OTA controls | I | C | C | C | C | A/R | C | I | C | R | I |
| Approve supplier evidence and obligations | I | C | C | C | C | C | C | I | A/R | I | I |
| Validate safety and quality evidence | I | C | C | R | A/R | C | C | C | C | I | I |
| Approve shadow-mode pilot | C | A | R | R | C | C | C | C | C | R | I |
| Approve launch or commissioning | A | R | C | C | C | C | C | C | C | I | C |
| Monitor model and data drift | I | A | R | C | C | C | C | C | I | R | I |
| Investigate operational incident | I | A | C | R | C | C | C | R | C | R | I |
| Activate fallback or rollback | I | A | C | R | C | C | I | R | I | R | I |
| Close Critical or High risk | A | R | C | C | C | C | C | C | C | I | C |
| Perform independent assurance | I | I | C | C | C | C | C | C | C | C | A/R |

## 4. Domain Notes

### Automotive

Domain Engineering includes ECU, ADAS, connected-vehicle, fleet, and OTA specialists. Safety and Quality participates in launch and Start of Production decisions. Cybersecurity is accountable for OTA integrity and connected-system controls.

### Wind Energy

Domain Engineering includes control and reliability engineers. Operations and Maintenance is responsible for turbine operating decisions, inspection, maintenance, and restricted operation. Commissioning remains a human governance decision.

## 5. Segregation of Duties

- The AI/Model Owner cannot be the sole approver of residual Critical or High risk.
- The person implementing a control cannot independently certify the control as effective.
- Privileged administrators cannot approve their own access exceptions.
- Supplier commercial ownership does not replace technical, cybersecurity, privacy, or quality review.
- Launch, commissioning, risk acceptance, and incident closure require the named accountable human role.

## 6. Escalation

Unresolved conflicts are escalated from the responsible role to the Product or Programme Leader, then to the Executive Risk Board for Critical exposure, major exceptions, or cross-functional deadlock. Legal or regulatory obligations follow the applicable organisational escalation path.
