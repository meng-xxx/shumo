# Q2F Final Inference Report

## Frozen final model

- Model: Q2D-R2-AV-MultiGap
- Model retraining: No
- Attachment3 labels used: No
- Pseudo-labeling: No

## Regression calibration

- Final intensity = clip(0.800000000 * raw_R2 + 0.009049484, -3, 3)

## Attachment3

- Samples: 30
- Negative: 8
- Neutral: 12
- Positive: 10

## Missing-mask contract

- Requested final policy: auto
- Explicit masks are preferred whenever present; otherwise Q2A-derived candidate missing masks are used under AUTO mode.
- Native numerical zeros are recorded separately and are not universally redefined as missing.

## Gates

- Frozen-BERT reproduction gate: PASS

## Main outputs

- Q2F_submission.csv
- Q2F_final_predictions.csv
- Q2F_mask_audit.csv
- Q2F_sensitivity_summary.csv