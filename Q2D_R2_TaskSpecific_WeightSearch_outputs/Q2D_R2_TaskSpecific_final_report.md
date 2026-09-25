# Q2D-R2 Task-Specific Weight Search Report

## Selected classification weights

- seed2026=0.7, seed2027=0.2, seed2028=0.1

## Selected regression weights

- seed2026=0.1, seed2027=0.0, seed2028=0.9

## Global affine calibration

- a=0.901000000
- b=-0.012816688

## Clean Validation

- Seed2028 raw: Acc=0.619505, F1=0.609812, MAE=0.576580, P=0.672229
- Task raw: Acc=0.633242, F1=0.622743, MAE=0.576359, P=0.672619
- Task OOF-cal: MAE=0.576118, P=0.669368

## Q2C2 Local-MultiGap

- Seed2028 raw: Acc=0.614072, F1=0.606055, MAE=0.576304, P=0.672093
- Task raw: Acc=0.624145, F1=0.613630, MAE=0.575970, P=0.672274
- Task OOF-cal: MAE=0.576229, P=0.669072

## Clean Test — reporting only

- Seed2028 raw: Acc=0.669876, F1=0.647682, MAE=0.616375, P=0.683248
- Task raw: Acc=0.661623, F1=0.636101, MAE=0.615975, P=0.684051
- Task global-cal: MAE=0.614323, P=0.684051

## Decision

- SELECT_TASK_SPECIFIC_WEIGHTED_ENSEMBLE

- Decision uses only Clean Validation + Q2C2. Test and Attachment3 are excluded from weight selection.