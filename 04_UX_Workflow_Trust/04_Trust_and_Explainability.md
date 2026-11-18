# Trust and Explainability

## Trust Approach

Trust is based on evidence, transparent limitations, reproducible evaluation, and accountable human control. A high confidence score or a plausible explanation is not sufficient proof that a model is correct or safe.

## Explanation Requirements

Every material model finding should answer:

1. What was detected or recommended?
2. Which evidence contributed to the finding?
3. Which model, dataset, software, prompt, or rule version was used?
4. What uncertainty or limitation applies?
5. Which intended-use boundary applies?
6. What may happen if action is taken or not taken?
7. What should the reviewer do next?
8. How can the decision be challenged or escalated?

## Explainability Methods

| Method | Suitable Use | Limitation |
|---|---|---|
| SHAP | Feature contributions for many tabular models | Contribution is not proof of causality |
| TCAV | Sensitivity to human-defined concepts | Depends on concept examples and model suitability |
| LIME | Local approximation around one prediction | Sensitive to sampling and local assumptions |
| Grad-CAM | Visual attention for some image models | A heatmap does not prove correct reasoning |
| Example-based explanation | Similar cases or scenarios | Similarity does not establish the same cause |
| Model Cards | Intended use, evaluation, and limitation records | Must remain complete and current |
| Data Sheets for Datasets | Dataset source, collection, composition, and constraints | Does not by itself prove lawful use or representativeness |

## Role-Based Explanations

- **Product leader:** enterprise impact, residual risk, unresolved controls, and decision request
- **Engineer:** model behaviour, test coverage, dataset, drift, version, and technical limitations
- **Operations reviewer:** recommendation, evidence, uncertainty, operating limits, and next action
- **Supplier reviewer:** model and data documentation, changes, incidents, audit rights, and exit exposure
- **Audit reviewer:** source evidence, versions, decision, rationale, approval, and control history

## Trust Controls

- Clearly label model-generated content.
- Keep original model output separate from human-edited output.
- Place evidence, uncertainty, and limitations near the recommendation.
- Do not preselect acceptance.
- Require justification for Critical and High decisions.
- Explain why a governance gate is blocked.
- Provide accept, reject, modify, request-evidence, and escalate actions.
- Preserve model, evidence, decision, and approval history.

## Evaluation

Explanation and trust evaluation should measure:

- Correct interpretation of the finding
- Ability to identify limitations
- Ability to locate supporting evidence
- Agreement with domain-expert review
- Decision time
- Acceptance, rejection, modification, and escalation patterns
- Over-reliance and under-reliance indicators
- False-positive and false-negative outcomes

## Common Trust Failures

- Plausible but unsupported explanations
- Outdated evidence or model versions
- Hidden uncertainty
- Misleading precision in risk or financial projections
- Explanations unsuitable for the reviewer
- Automation bias
- Selective reporting of successful tests
- Failure to revalidate after a material change
