# Q2E Classical R1 Strong Baseline Report

## Design

- Text: Frozen-BERT CLS + masked mean
- Audio: preserve all 50x74 temporal positions + mean/std/max
- Vision: preserve all 50x35 temporal positions + mean/std/max
- Feature dimension: 7313
- Attachment3 used: No
- Q2C used for hyperparameter selection: No

## Selected Hyperparameters

- SVC C: 1.0
- Ridge alpha: 30000.0
- Ridge best alpha is upper-grid boundary: False

## Clean Validation

- Accuracy: 0.590659
- Macro-F1: 0.571460
- MAE: 0.654995
- Pearson: 0.552325

## Clean Test

- Accuracy: 0.642366
- Macro-F1: 0.595837
- MAE: 0.700595
- Pearson: 0.616800

## Task-Matched A/V Robustness

- Mean Accuracy: 0.585409
- Mean Macro-F1: 0.571084
- Mean MAE: 0.650592
- Mean Pearson: 0.562954
- Worst Accuracy: 0.565934

## General 90-Scenario Stress Test

- Mean Accuracy: 0.552259
- Mean Macro-F1: 0.536850
- Mean MAE: 0.663835
- Mean Pearson: 0.530851
- Worst Accuracy: 0.387363