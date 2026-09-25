# Q2D-R2 Three-Seed Ensemble Report

## Contract

- No neural-network training.
- Frozen seeds: 2026 / 2027 / 2028.
- Equal sample-level ensemble weights: 1/3 each.
- Attachment3 not used.
- Test not used for model selection.

## Clean Validation — Raw

- Seed 2028: Acc=0.619505, F1=0.609812, MAE=0.576580, Pearson=0.672229
- Ensemble: Acc=0.623626, F1=0.612277, MAE=0.584711, Pearson=0.668464

## Q2C2 Local-MultiGap — Raw

- Seed 2028: Acc=0.614072, F1=0.606055, MAE=0.576304, Pearson=0.672093
- Ensemble: Acc=0.622711, F1=0.611833, MAE=0.584087, Pearson=0.668297

## Q2C2 Local-MultiGap — Validation-OOF Calibration

- Seed 2028 calibrated MAE/Pearson: 0.576710 / 0.669242
- Ensemble calibrated MAE/Pearson: 0.573073 / 0.666148

## Clean Test — Reporting Only

- Seed 2028 raw: Acc=0.669876, F1=0.647682, MAE=0.616375, Pearson=0.683248
- Ensemble raw: Acc=0.665750, F1=0.642313, MAE=0.627043, Pearson=0.686029

## Decision

- KEEP_SEED_2028_SINGLE_REFERENCE
- Decision uses only Clean Validation + Q2C2; the Test metrics above are not part of the gate.

See Q2D_R2_ThreeSeed_bootstrap_summary.csv for paired uncertainty estimates.