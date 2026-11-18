# Cost to Serve and Unit Economics

## 1. Purpose

This document defines the cost structure and unit-economics model for RiskReview AI. Current figures are planning assumptions and should be replaced with supplier quotes and pilot measurements.

## 2. Proposed ₹10 Crore Investment Allocation

| Module | Indicative Investment | Main Scope |
|---|---:|---|
| Data foundation and connectors | ₹2.00 crore | Risk-register ingestion, evidence links, lineage, data quality, and domain connectors |
| AI and rules engine | ₹2.25 crore | Deterministic checks, contextual analysis, related-risk detection, and challenge questions |
| Responsible AI and Explainable AI | ₹1.25 crore | Model Cards, Data Sheets, SHAP/TCAV support, uncertainty, and limitation displays |
| Human–AI workflow and governance gates | ₹1.25 crore | Review, override, escalation, segregation of duties, and Go/No-Go controls |
| Monitoring, audit, and cybersecurity | ₹1.75 crore | Drift, incidents, access, versioning, audit trail, and operational monitoring |
| Integration, pilot, change, and contingency | ₹1.50 crore | Enterprise integration, shadow-mode pilot, training, support, and contingency |
| **Total** | **₹10.00 crore** | Six-module platform and rollout |

## 3. Annual Operating-Cost Categories

- Cloud or on-premises compute and storage
- Model inference and monitoring
- Data ingestion and connector maintenance
- Security operations, vulnerability review, and audit logging
- Domain-expert and human-review effort
- Customer support and implementation
- Model, prompt, rule, and dataset maintenance
- Independent assurance and periodic control testing
- Licensing for third-party models, observability, or security tools

A working planning range is **15%–30% of initial platform investment per year**, or approximately **₹1.5–₹3.0 crore annually**, until real supplier and staffing estimates are available.

## 4. Cost-to-Serve Unit

The initial commercial unit is one controlled enterprise deployment covering:

- One approved automotive programme, fleet, plant, or wind-energy asset group
- Up to an agreed number of authorised users
- One domain configuration
- A defined volume of risk records and evidence
- Standard reporting, monitoring, and support

## 5. Unit Cost Formula

**Annual Cost to Serve per Customer = Allocated Platform Operations + Customer-Specific Infrastructure + Support + Domain Review + Integration Amortisation + Assurance Cost**

Worked planning example:

| Cost Element | Example Annual Amount |
|---|---:|
| Allocated platform operations | ₹20 lakh |
| Customer-specific infrastructure and model usage | ₹15 lakh |
| Support and customer success | ₹12 lakh |
| Domain review and assurance | ₹18 lakh |
| Integration amortisation | ₹15 lakh |
| Security and audit support | ₹10 lakh |
| **Illustrative annual cost to serve** | **₹90 lakh** |

This example is not a quotation or achieved cost.

## 6. Contribution Margin

**Contribution Margin = Annual Contract Value − Annual Variable Cost to Serve**

**Contribution Margin % = Contribution Margin ÷ Annual Contract Value × 100**

Example at an annual contract value of **₹1.50 crore** and annual cost to serve of **₹90 lakh**:

- Contribution margin = ₹1.50 crore − ₹0.90 crore = **₹60 lakh**
- Contribution margin percentage = ₹60 lakh ÷ ₹1.50 crore = **40%**

A mature software-led model should target a higher contribution margin after integration and domain-review effort become repeatable. The initial pilot may have a lower or negative margin because discovery, integration, and assurance effort is concentrated upfront.

## 7. Break-Even Customer Count

**Break-Even Customers = Annual Fixed Operating Cost ÷ Contribution Margin per Customer**

Example:

- Annual fixed operating cost: ₹2.40 crore
- Contribution margin per customer: ₹60 lakh
- Break-even customer count: ₹2.40 crore ÷ ₹0.60 crore = **4 customers**

This excludes recovery of the initial ₹10 crore platform investment. Full investment recovery requires cumulative contribution margin across customers and years.

## 8. Cost-Control Levers

- Standardise the risk schema and connectors
- Reuse domain templates without assuming identical thresholds
- Route only material findings to expensive human review
- Cache or batch non-urgent model analysis
- Use deterministic rules for explicit checks
- Limit high-cost explainability methods to appropriate cases
- Automate evidence lineage and audit reporting
- Monitor model usage and remove low-value prompts or duplicate processing

## 9. Unit-Economics Validation

During the pilot, record:

- Integration hours
- Cloud and inference consumption
- Support hours
- Domain-review hours
- Security and assurance effort
- Risk records processed
- Material findings reviewed
- Time saved compared with baseline
- Customer willingness to pay

Unit economics should be recalculated after each pilot and before commercial scale.
