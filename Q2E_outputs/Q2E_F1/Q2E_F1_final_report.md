# Q2E-F1 Final Report

## Scope

- No new neural-network training.
- Attachment3 not used.
- Q2C2 is a Local-MultiGap A/V benchmark with 45 fixed scenarios.
- Validation/Q2C2 calibration metrics use sample-level 5-fold OOF coefficients.
- Global affine coefficients are saved only for future unseen samples.

## Q2C2 Raw

- Q2B: Acc=0.609737, Macro-F1=0.603134, MAE=0.585545, Pearson=0.650325
- Q2D-R2: Acc=0.621184, Macro-F1=0.610439, MAE=0.588146, Pearson=0.662859

## Q2D-R2 OOF Calibration on Q2C2

- MAE: 0.588146 -> 0.573816
- Pearson: 0.662859 -> 0.661151

## Statistical Check

- Raw Q2C2 R2-vs-Q2B MAE delta CI excludes zero: False

## Decision

- Calibration helpful for R2: True
- R2 classification better than Q2B on Q2C2: True
- Recommended final variant: Q2D_R2_with_global_affine_calibration

See Q2E_F1_bootstrap_summary.csv and Q2E_F1_final_comparison.csv for full numerical results.