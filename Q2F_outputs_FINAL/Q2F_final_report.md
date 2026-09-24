# Q2F Final Inference Report

## Frozen final model

- Model: Q2D-R2-AV-MultiGap
- Q2F terminal-aware mask correction: Enabled
- Model retraining: No
- Attachment3 labels used: No
- Pseudo-labeling: No

## Regression calibration

- Final intensity = clip(0.800000000 * raw_R2 + 0.009049484, -3, 3)

## Attachment3

- Samples: 30
- Negative: 9
- Neutral: 11
- Positive: 10

## Missing-mask contract

- Requested final policy: auto
- Explicit masks are preferred whenever present; otherwise terminal-aware Q2A-derived candidate masks are used under AUTO mode.
- The model content mask remains attention_mask > 0; only the last attended position is excluded from missing detection.
- Native numerical zeros are recorded separately and are not universally redefined as missing.

## Gates

- Frozen-BERT reproduction gate: PASS
- Terminal-aware missing-mask gate: PASS
- Audited mean missing rate A/V: 0.2548 / 0.2578

## Main outputs

- Q2F_submission.csv
- Q2F_final_predictions.csv
- Q2F_mask_audit.csv
- Q2F_sensitivity_summary.csv