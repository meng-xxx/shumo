# Q2D-R2 Hybrid Final Candidate Confirmation

## Frozen hybrid

- Classification: Seed 2028 only.
- Regression: 0.1×Seed2026 + 0.9×Seed2028.
- No new training.
- No weight search.
- Attachment3 not used.

## Global calibration

- Hybrid: a=0.901000000, b=-0.012816688
- Seed2028 reference: a=0.909000000, b=-0.013608474

## Clean Validation

- Seed2028 raw: Acc=0.619505, F1=0.609812, MAE=0.576580, P=0.672229
- Hybrid raw: Acc=0.619505, F1=0.609812, MAE=0.576359, P=0.672619
- Seed2028 OOF MAE/P=0.576561/0.669334
- Hybrid OOF MAE/P=0.576118/0.669368

## Q2C2 Local-MultiGap

- Seed2028 raw: MAE=0.576304, P=0.672093
- Hybrid raw: MAE=0.575970, P=0.672274
- Seed2028 OOF: MAE=0.576710, P=0.669242
- Hybrid OOF: MAE=0.576229, P=0.669072

## Clean Test — reporting only

- Seed2028 global: Acc=0.669876, F1=0.647682, MAE=0.615296, P=0.683248
- Hybrid global: Acc=0.669876, F1=0.647682, MAE=0.614323, P=0.684051

## Final decision

- SELECT_HYBRID_FINAL_CANDIDATE

- Decision uses Clean Validation + Q2C2 only. Test is reporting-only and Attachment3 is excluded.