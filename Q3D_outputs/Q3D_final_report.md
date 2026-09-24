# Q3D Final Explainer Freeze & Evidence Validation

- Decision: **PASS_FINAL_EXPLAINER_FROZEN**
- Frozen formal baseline: **NEUTRAL_ZERO**
- Baseline was not reselected.
- BERT replay median cosine: 0.99999998
- Corrected Shapley/local Top-1 agreement: 0.755; Spearman: 0.602; L1: 0.450
- Corrected local non-degenerate fraction: 1.000
- Frozen NMS threshold: 0.3
- Formal Top-K gains remain positive for classification and regression: True
- Natural-zero maximum repeated-zero effect: 0
- Stability labels: {'Moderate': 367, 'High': 229, 'Low': 132}

Text evidence uses whole-word WordPiece masking followed by Frozen BERT recomputation. Audio/Vision use normalized-input neutral-zero temporal occlusion. Contributions describe model input/decision contribution, not causal emotion generation.

Q3E permission: allowed. Attachment4 formal inference was not run.
