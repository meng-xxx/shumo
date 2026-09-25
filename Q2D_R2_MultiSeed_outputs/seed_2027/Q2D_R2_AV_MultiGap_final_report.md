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

- Training seed: 2027
- Best epoch: 7
- Best selection score: 0.676860
- Epochs run: 15

## Clean Validation

- Accuracy: 0.627747
- Macro-F1: 0.617581
- MAE: 0.604272
- Pearson: 0.660024

## Clean Test

- Accuracy: 0.656121
- Macro-F1: 0.631618
- MAE: 0.649656
- Pearson: 0.685130

## Task-Matched A/V Robustness vs Q2B

- Mean Accuracy gain: +0.019048
- Mean Macro-F1 gain: +0.014869
- Mean MAE reduction: -0.019589
- Mean Pearson gain: +0.009148
- Q2B worst Accuracy: 0.585165
- R1 worst Accuracy: 0.614011
- Model gate: **PARTIAL**

## General 90-Scenario Stress Test vs Q2B

- Mean Accuracy gain: +0.004655
- Mean Macro-F1 gain: +0.005321
- Mean MAE reduction: -0.007736
- Mean Pearson gain: +0.002439

The task-matched A/V result is the primary Q2D-R2-AV-MultiGap robustness result;
the full 90-scenario Q2C result is retained as a broader stress test.