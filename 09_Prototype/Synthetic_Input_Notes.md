# Synthetic Input Notes

## Purpose
The dataset expands the prototype beyond one or two static examples and demonstrates input coverage across ten automotive programme workstreams.

## Dataset
- 12 synthetic risks
- 10 workstreams
- 7 high-severity and 5 medium-severity examples
- 2 deliberately old evidence dates for rule-check demonstration
- Cause, impact, owner, target date, mitigation and evidence fields

## Use in the app
1. Open `app/index.html`.
2. Select **Synthetic inputs**.
3. Select **Load built-in 12-risk dataset**, or choose `Synthetic_Risk_Register.csv`.
4. Review the preview table.
5. Continue to Dashboard, Risk finding, Related risks and Mitigation challenge.

## Important boundary
The input data and dashboard outputs are illustrative. The static MVP does not retrain a model or recalculate all findings from the CSV. CSV loading occurs locally in the browser and is intended to demonstrate the input contract and review workflow.
