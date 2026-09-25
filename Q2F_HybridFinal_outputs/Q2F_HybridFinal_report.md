# Q2F HybridFinal Attachment3 Final Inference

## Frozen predictor

- Classification: Q2D-R2 Seed 2028 only.
- Regression: 0.1×Seed2026 + 0.9×Seed2028.
- Calibration: y_final = clip(0.901000000000 × y_raw -0.012816688156, -3, 3).
- No training, pseudo-labeling, label use, or weight search on Attachment3.

## Terminal-aware mask audit

- Mean audited A missing rate: 0.254819
- Mean audited V missing rate: 0.257849
- Terminal A-zero count: 30/30
- Terminal V-zero count: 30/30

## Final outputs

- Samples: 30
- Class counts: {'Negative': 9, 'Neutral': 11, 'Positive': 10}
- Intensity mean/std: 0.098394 / 0.578349
- Intensity range: [-1.150417, 1.529970]

Primary submission file:
`Q2F_HybridFinal_submission.csv`