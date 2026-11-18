# RiskReview AI - Initial Automotive Programme Risk Review Workflow

Paste the following PlantUML source into the official PlantUML Web Server and export the result as PNG or SVG.

```plantuml
@startuml
skinparam backgroundColor white
skinparam shadowing false
skinparam defaultFontName Arial
skinparam defaultFontSize 12
skinparam activity {
  BackgroundColor #F7F7F7
  BorderColor #555555
  DiamondBackgroundColor #FFF4CC
  DiamondBorderColor #555555
  StartColor #222222
  EndColor #222222
}

title Enterprise AI Risk Governance and Assurance Workflow

|Product or Risk Owner|
start
:Select automotive AI/ECU or
wind-turbine use case;
:Create or update enterprise AI risk;
:Add impact, owner, proposed control,
due date and supporting evidence;

|RiskReview AI Model|
:Validate mandatory fields, dates,
score ranges and evidence references;
:Review cause-event-impact structure;
:Analyse model, data, supplier,
cybersecurity and operational indicators;
:Identify potentially related risks;
:Generate control challenge questions;
:Present finding, rationale,
uncertainty and limitations;

|Domain and Governance Reviewer|
:Review model finding and source evidence;
if (Information or evidence complete?) then (No)
  :Return finding to Product or Risk Owner;
  |Product or Risk Owner|
  :Add or correct information and evidence;
  |RiskReview AI Model|
  :Refresh validation and model finding;
  |Domain and Governance Reviewer|
else (Yes)
endif

if (Related risk suggested?) then (Yes)
  :Compare risk records and evidence;
  if (Same underlying risk?) then (Yes)
    :Recommend merge for human confirmation;
  else (No)
    :Recommend link or keep separate;
  endif
else (No)
endif

:Approve likelihood and impact inputs;

|Governance Decision Authority|
:Review finding, evidence,
uncertainty and recommendation;
:Accept, modify, reject, link,
merge, defer or escalate;
:Record decision rationale;
:Apply 5x5 risk tier and governance gate;
if (Critical or unresolved High risk?) then (Yes)
  :Block or restrict launch/commissioning;
  :Approve mitigation, exception,
restricted operation or revalidation;
else (No)
  :Permit controlled progression
with required monitoring;
endif

|Audit and Monitoring Service|
:Record risk, evidence, rule/model finding,
versions, decision, approver and timestamp;
:Monitor drift, incidents,
fairness and control performance;
if (Material change detected?) then (Yes)
  :Trigger reassessment and human reapproval;
else (No)
  :Continue approved monitoring;
endif
stop

legend bottom
  RiskReview AI is a human-supervised decision-support model.
  Expected efficiency and cost benefits require controlled-pilot validation.
  Authorised humans retain final risk, launch and commissioning authority.
endlegend
@enduml

```

## Repository placement

- Source: `04_UX_Workflow_Trust/01_Initial_Workflow_PlantUML.md`
- Rendered image: `04_UX_Workflow_Trust/Images/01_Initial_Workflow_PlantUML.png`
