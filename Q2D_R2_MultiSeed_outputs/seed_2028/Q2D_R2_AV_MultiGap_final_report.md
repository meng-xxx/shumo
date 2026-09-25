# Q2D-R2-AV-MultiGap Report

## Design

- Text synthetic missing: No
- Audio local block missing: Yes
- Vision local block missing: Yes
- Audio+Vision synchronized block missing: Yes
- Native A/V zeros automatically treated as missing: No
- Frozen Q2B teacher: Yes
- Frozen Q2B encoders for first 3 epochs
- Encoder LR after unfreeze: 2e-05
- New-module LR: 0.0002
- Attachment3 used: No
- Q2C 90-scenario benchmark used for early stopping: No

## Training

- Training seed: 2028
- Best epoch: 3
- Best selection score: 0.676146
- Epochs run: 11

## Clean Validation

- Accuracy: 0.619505
- Macro-F1: 0.609812
- MAE: 0.576580
- Pearson: 0.672229

## Clean Test

- Accuracy: 0.669876
- Macro-F1: 0.647682
- MAE: 0.616375
- Pearson: 0.683248

## Task-Matched A/V Robustness vs Q2B

- Mean Accuracy gain: +0.005983
- Mean Macro-F1 gain: +0.004749
- Mean MAE reduction: +0.009811
- Mean Pearson gain: +0.020235
- Q2B worst Accuracy: 0.585165
- R1 worst Accuracy: 0.601648
- Model gate: **PASS_STRICT**

## General 90-Scenario Stress Test vs Q2B

- Mean Accuracy gain: -0.007082
- Mean Macro-F1 gain: -0.000885
- Mean MAE reduction: +0.009412
- Mean Pearson gain: +0.012149

The task-matched A/V result is the primary Q2D-R2-AV-MultiGap robustness result;
the full 90-scenario Q2C result is retained as a broader stress test.