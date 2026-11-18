# RiskReview AI - Initial Automotive Programme Risk Review Workflow

Paste the following PlantUML source into the official PlantUML Web Server and export the result as PNG or SVG.

```plantuml
@startuml
' RiskReview AI - Initial Automotive Programme Risk Review Workflow
skinparam backgroundColor white
skinparam shadowing false
skinparam defaultFontName Arial
skinparam defaultFontSize 12
skinparam activity {
  BackgroundColor #F7F7F7
  BorderColor #666666
  DiamondBackgroundColor #FFFFFF
  DiamondBorderColor #666666
  StartColor #222222
  EndColor #222222
  BarColor #666666
}
skinparam partition {
  BackgroundColor white
  BorderColor #333333
  FontColor #111111
}

title RiskReview AI - Initial Automotive Programme Risk Review Workflow

|Risk Owner|
start
:Create or update programme risk;
:Add cause, uncertain event and impact;
:Add owner, mitigation and due date;
:Add supporting evidence and review date;

|RiskReview AI|
:Validate mandatory fields;
:Check date format and overdue actions;
:Check evidence freshness;
:Review cause-event-impact structure;
:Identify potentially related risks;
:Generate mitigation challenge questions;
:Present finding, reason and uncertainty;

|APQP Coordinator|
:Review AI finding and supporting evidence;
if (Information incomplete?) then (Yes)
  :Return finding to Risk Owner;
  |Risk Owner|
  :Add missing information or evidence;
  |RiskReview AI|
  :Refresh checks and finding;
  |APQP Coordinator|
else (No)
endif

if (Related risk suggested?) then (Yes)
  :Compare both risk entries;
  if (Same underlying risk?) then (Yes)
    :Recommend merge for human confirmation;
  else (No)
    :Recommend link or keep separate;
  endif
else (No)
endif

|NPD Project Manager|
:Review finding, evidence and recommendation;
:Accept, edit, reject, link, merge or defer;
:Record reason for the decision;
:Confirm verified programme-review agenda;

|Audit Service|
:Record original risk text;
:Record rule or AI finding;
:Record model, prompt or rule version;
:Record human decision and rationale;
:Record reviewer and timestamp;
stop

legend bottom
  Human decision authority is retained by the APQP Coordinator and NPD Project Manager.
  RiskReview AI provides validation, analysis, challenge questions and related-risk suggestions only.
endlegend
@enduml
```

## Repository placement

- Source: `04_UX_Workflow_Trust/01_Initial_Workflow_PlantUML.md`
- Rendered image: `04_UX_Workflow_Trust/Images/01_Initial_Workflow_PlantUML.png`
