# Q3 HybridFinal Final Packaging Audit

Decision: **PASS_Q3_HYBRID_FINAL_WITH_PACKAGING_WARNINGS**

## Frozen contract
- Classification: Seed2028
- Regression: 0.1×Seed2026 + 0.9×Seed2028
- Calibration: clip(0.901 × y_raw -0.012816688156128, -3, 3)
- No prediction, Shapley value, or evidence score was modified.

## Final summary
- Samples: 20/20
- Classes: {'Positive': 9, 'Negative': 7, 'Neutral': 4}
- Classification primary modality: {'T': 20}
- Regression primary modality: {'T': 15, 'V': 4, 'A': 1}
- Native-zero Vision samples: ['13']
- Class/regression disagreement samples: ['02']
- Mapping-partial samples: ['09', '15']

## Interpretation semantics
Primary HybridFinal attribution is **missing-aware** and is interpreted as model
sensitivity to modality/segment availability. The zero baseline remains an auxiliary
stability reference.

For native-all-zero Vision samples, non-zero missing-aware Vision effects are labelled
**availability-state sensitivity only**. No visual-content evidence is claimed or shown.

## Mapping/display audit
- Zero/short duration threshold: <= 0.020 s
- Source zero/short-duration evidence rows: 7
- Zero-duration text phrases are kept but their timestamps are suppressed.
- Zero-duration Audio/Vision intervals are suppressed from final display.
- Frame copy failures: None

## Fidelity inherited from HybridFinal
- Classification Top-K − Random-K mean: 0.154403,
  95% CI [0.099057, 0.215738]
- Regression Top-K − Random-K mean: 0.242976,
  95% CI [0.128832, 0.370572]

## Highest classification entropy samples
```text
sample_id predicted_class  hybrid_final_intensity  normalized_entropy  probability_margin task_consistency
       02        Positive               -0.181182            0.991567            0.073343         DISAGREE
       19        Positive                0.370416            0.959912            0.058875            AGREE
       04        Negative               -0.049274            0.886221            0.309237            AGREE
       03         Neutral               -0.038808            0.865812            0.192297    NEUTRAL_CLASS
       18        Negative               -0.408896            0.838106            0.222204            AGREE
```

Interpretations describe model decision evidence/sensitivity. They do not establish
causal emotion generation and do not prove prediction correctness.
