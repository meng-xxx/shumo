# Q2E TextAnchor-NoComp Core Ablation Report

## Contract

- Attachment3 used: No
- Q2C used for training/early stopping: No
- Text synthetic missing: No
- Native A/V zero treated as missing: No
- Validation missing distribution fixed across variants: Yes

## Variants

- text_anchor_nocomp: full TextAnchor NoComp model
- no_availability_context: binary visibility only
- no_consistency_teacher: removes consistency + teacher constraints
- longblock_only: removes MultiGap training

## Replacement rule

TextAnchor replaces R2 only if task MAE improves and task Accuracy/Macro-F1/Pearson remain within 0.002 of R2, while worst Accuracy remains within 0.005.

- Replacement candidate: None

See Q2E_TextAnchor_ablation_summary.csv for the complete metric table.