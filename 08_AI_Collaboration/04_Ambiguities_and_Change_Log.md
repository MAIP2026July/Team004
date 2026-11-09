# Ambiguities and Change Log

## Open Ambiguities

| ID | Ambiguity | Why It Matters | Owner | Resolution Evidence | Status |
|---|---|---|---|---|---|
| A-01 | Final economic buyer | Determines value proposition and pricing | Swaminathan B. | Buyer interviews | Open |
| A-02 | Standard risk-register schema | Affects upload, validation, and configuration | Maharshi Pandit | Target-user review | Open |
| A-03 | Evidence-age threshold | Different risk categories may need different rules | Joint | Labelled examples and user validation | Open |
| A-04 | Related-risk threshold | Affects false merge suggestions | Maharshi Pandit | Held-out evaluation | Open |
| A-05 | Hosting and model provider | Affects privacy, cost, and fallback | Joint | Architecture decision | Open |
| A-06 | Paid-pilot price | Required for revenue roadmap | Swaminathan B. | Willingness-to-pay interviews | Open |

## Important Changes Already Made

| Change | Reason | Impact |
|---|---|---|
| Narrowed from cross-industry to automotive component NPD/NPI | Professor required a specific industry and segment | All artifacts use APQP-to-Start-of-Production scope |
| Defined monthly programme-risk review as the first workflow | Prevents an overly broad product | MVP and prototype remain focused |
| Restored programme-risk scope after warranty-claim drift | Warranty claims are a different product and user workflow | Removed claim-triage framing |
| Separated deterministic rules, AI assistance, and human decisions | Improves reliability and accountability | Architecture and UX show clear boundaries |
| Added PlantUML initial swimlane | Professor requested an initial textual workflow | Workflow can be version-controlled and updated |
| Added MVP-to-revenue roadmap | Professor requested a route from MVP to money | Paid pilot precedes recurring subscription |
| Added AI build prompt and self-evaluation | Professor requested AI product build and critical evaluation | Repository documents AI use and human corrections |

## Change-Control Rule

A material change to industry, segment, workflow, primary user, human authority, data source, model provider, thresholds, or commercial model must be recorded in the Product Decision Log and reflected across affected Markdown artifacts.
