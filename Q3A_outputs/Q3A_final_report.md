# Q3A — Attachment 4 + Final Q2 Model Interface Audit

Generated: 2026-09-24T17:45:12

## 1. Decision

**WARN**

Final frozen Q2 predictor:

`Q2D-R2-AV-MultiGap + Global Affine Calibration`

Q3A executed **no training, no Attachment 4 prediction, no pseudo-label generation, and no Attachment 4 performance evaluation**.

## 2. Final Q2 model contract

- R2 checkpoint: `D:\Desktop\shumo\E题数据\Q2D_R2_AV_MultiGap_outputs\checkpoints\Q2D_R2_AV_MultiGap_best_model.pt`
- Checkpoint exists: `True`
- Normalization: `D:\Desktop\shumo\E题数据\Q2B_outputs\Q2B_normalization_stats.npz`
- Normalization exists: `True`
- Global affine calibration: `D:\Desktop\shumo\E题数据\Q2E_outputs\Q2E_F1\Q2E_F1_global_calibration.json`
- Calibration: `a=0.8`, `b=0.009049484` (authoritative frozen Q2 contract)
- Final regression contract: `clip(a * raw_R2_regression + b, -3, 3)`

## 3. Attachment 4 aligned features

- PKL files found: **20**
- Expected: **20**
- Successfully audited: **20**
- Unique sample IDs: **20**
- Duplicate IDs: `[]`
- Files with label-like field names: **0**
  - These values were ignored and never exported/used.
- Samples with A/V native zero run >= 3: **1**
  - Native numerical zero is **not** treated as missing.

## 4. Raw-video pairing

- Video files found: **20**
- Samples uniquely paired to a video: **20/20**
- Samples ready for Q1 time-mapping reuse: **20/20**

Q3A only checks mapping prerequisites. The actual
`aligned position -> text/word -> audio time -> video frame`
mapping is generated in the next stage by reusing the finalized Q1 alignment procedure on Attachment 4.

## 5. Hard failures

- None

## 6. Warnings

- A calibration artifact was found but its schema could not be parsed automatically. Q3A still uses the already-frozen Q2 final coefficients a=0.8, b=0.009049484.
- 1 samples contain A/V all-zero runs of length >= 3 inside text-defined valid positions. Per the frozen Q2 contract, native numerical zero != missing; these are reported for audit only and are NOT converted into missing masks.

## 7. Outputs

- `Q3A_feature_audit.csv`
- `Q3A_video_audit.csv`
- `Q3A_id_pairing.csv`
- `Q3A_mapping_feasibility.csv`
- `Q3A_position_mapping_template.csv`
- `Q3A_model_contract.json`
- `Q3A_frozen_global_affine_calibration.json`
- `Q3A_input_manifest.csv`
- `Q3A_summary.json`
- `Q3A_gate.json`
- `Q3A_run_config.json`

## 8. Stop condition

If Q3A is `FAIL`, do **not** start Q3B/Shapley/occlusion.
Fix the failed data/model-interface gate first.

If Q3A is `PASS` or only contains understood non-fatal `WARN`s,
the next stage is Q3B:
frozen final-model clean reproduction + coalition/Shapley feasibility audit.
