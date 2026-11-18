# Scaling Strategy and Constraints

## 1. Scaling Principle

Scale only after a controlled pilot demonstrates technical quality, human-governance effectiveness, secure data handling, workflow value, and sustainable cost to serve.

## 2. Scaling Sequence

### Phase 1: Single Automotive Workflow

- One programme or product line
- Standardised risk schema
- Human-supervised shadow mode
- Manual or limited integrations

### Phase 2: Automotive Portfolio

- Multiple ECU, ADAS, connected-vehicle, or OTA programmes
- Shared governance taxonomy
- Portfolio reporting
- Supplier evidence workflows

### Phase 3: Enterprise Automotive Deployment

- Multiple programmes, plants, fleets, and suppliers
- Role-based access and segregation of duties
- Enterprise integrations
- Independent assurance and operational support

### Phase 4: Wind-Energy Configuration

- Separate turbine, sensor, maintenance, and control taxonomy
- Wind-energy-labelled evaluation set
- Domain-specific thresholds and reviewers
- Controlled asset-group pilot

### Phase 5: Multi-Domain Platform

- Common governance core
- Domain-specific data models, prompts, rules, controls, and evaluation
- Shared portfolio reporting without assuming identical risk meaning

## 3. Reusable Platform Components

- Identity, access, and audit services
- Evidence lineage and versioning
- Human review and escalation workflow
- Risk calculation and gate engine
- Model and data monitoring
- Reporting and export
- Supplier evidence-management pattern

## 4. Domain-Specific Components

### Automotive

- ECU and ADAS operating conditions
- Fleet telemetry and incidents
- OTA release and rollback evidence
- Supplier model and hardware information
- Launch and Start of Production gates

### Wind Energy

- SCADA and condition-monitoring data
- Sensor calibration and maintenance history
- Wake-steering and control-model evidence
- Turbine, site, weather, and operational context
- Maintenance and commissioning gates

## 5. Scaling Constraints

| Constraint | Effect | Mitigation |
|---|---|---|
| Confidential and proprietary data | Limits training and evaluation | Synthetic data, anonymisation, private deployment, approved access |
| Different risk taxonomies | Reduces portability | Common core schema plus domain mappings |
| Small labelled datasets | Weak performance evidence | Phased data collection and independent labelling |
| Supplier opacity | Missing model and change evidence | Contractual Glass-Box requirements and audit rights |
| Integration complexity | Increases cost and timeline | Standard connectors and bounded pilot scope |
| Human-review capacity | Creates bottleneck | Prioritise material findings and route by expertise |
| Regulatory variation | Requires localisation | Maintain jurisdiction-specific control mappings |
| Automation bias | Weakens human accountability | Explanation, uncertainty, override, and review analytics |
| Model and data drift | Performance changes after deployment | Continuous monitoring and revalidation triggers |
| High cost to serve | Weakens unit economics | Reusable modules, deterministic checks, and implementation standards |

## 6. Scale Gates

A new programme, site, fleet, or domain should not be added until:

- Data owner, business owner, and governance authority are named
- Intended and prohibited uses are documented
- Security, privacy, and supplier controls are approved
- Representative evaluation data is available
- Human review and escalation capacity is confirmed
- Monitoring, incident, rollback, and revalidation processes are operational
- Unit economics remain within the approved range

## 7. Operating Model

A scaled service requires:

- Product and platform management
- Data engineering and governance
- AI and rules engineering
- MLOps and observability
- Cybersecurity and privacy
- Automotive and wind-energy domain experts
- Customer implementation and support
- Independent model risk or internal audit review

## 8. Scaling Metrics

- Time to configure a new programme or site
- Percentage of reusable versus custom components
- Customer implementation hours
- Annual cost to serve
- Contribution margin
- Model performance by domain
- Human-review workload
- Incident and revalidation volume
- Renewal, expansion, and customer adoption

## 9. Exit or Stop Conditions

Pause or stop scaling when Critical errors remain unresolved, human-review capacity is insufficient, data access is not compliant, security controls fail, cost to serve consistently exceeds commercial value, or the customer cannot maintain final human accountability.
