# Cost-to-Serve and Unit Economics

## Cost Categories

### Variable Costs

- Model or API inference per risk entry
- Embedding or similarity processing
- Storage and logging
- Notification or export services
- Human verification effort during a managed pilot

### Fixed and Semi-Fixed Costs

- Product development and testing
- Customer onboarding and configuration
- Security and access-control implementation
- Monitoring and evaluation
- Support and incident response
- Prompt, rules and model maintenance
- Automotive taxonomy configuration

## Unit of Analysis

The preferred early unit is **one reviewed programme risk register per monthly review cycle**. Alternative units to validate are active programme, reviewer seat and annual enterprise subscription.

## Unit-Economics Formula

```text
Contribution per reviewed register
= recognised revenue per register
- model/API cost
- infrastructure cost
- allocated human review cost
- allocated support cost
```

## Pilot Cost Sheet

| Cost Item | Calculation Method | Evidence Status |
|---|---|---|
| AI processing | Entries × calls per entry × provider rate | TBD |
| Storage and logs | Data volume × retention period | TBD |
| Human verification | Reviewer minutes × loaded rate | Requires pilot |
| Configuration | Team hours × loaded rate | Requires scope |
| Support | Support hours per programme | Requires pilot |
| Security and integration | Customer-specific estimate | Out of prototype scope |

## Cost Controls

- Use deterministic rules before model calls.
- Batch semantic analysis when safe.
- Use smaller approved models for simple classification.
- Restrict retries and uncontrolled agent loops.
- Cache only non-sensitive derived results where permitted.
- Route low-confidence findings to human review rather than repeated generation.
- Monitor cost per useful accepted or edited finding.

## Economic Guardrail

The paid pilot should not proceed to a recurring contract unless the team can estimate cost per programme review, human-review burden and a plausible gross-margin path.
