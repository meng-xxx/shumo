# Q3C Local Attribution, Faithfulness & Baseline Selection

- Decision: **PASS_NEUTRAL_ZERO_PRIMARY_BASELINE_SENSITIVE**
- Final Q3 baseline: **NEUTRAL_ZERO**
- Why: paired CI crosses zero; neutral-zero is preferred for input-information semantics, natural-zero idempotence, and avoidance of missing-state effects

## Required conclusions

1. Selected baseline: NEUTRAL_ZERO.
2. Selection rationale: paired CI crosses zero; neutral-zero is preferred for input-information semantics, natural-zero idempotence, and avoidance of missing-state effects
3. Top-K vs Random-K: classification comprehensiveness: mean=0.5649, CI-low=0.518, regression comprehensiveness: mean=0.1538, CI-low=0.1393, classification sufficiency: mean=0.4735, CI-low=0.4317, regression sufficiency: mean=0.1425, CI-low=0.1271. All four gain CIs are above zero; VALID label metrics support Top-K over Random-K at all three K ratios=True.
4. Classification/regression support: classification=yes; regression=yes.
5. Shapley/local consistency: Top-1=0.699, mean Spearman=0.051, mean L1=0.689. Within-modality normalization makes local modality sums frequently tied; interpret this diagnostic cautiously.
6. Multiscale stability: moderate and scale-dependent; mean Top-20% Jaccard=0.431, mean position Spearman=0.507. Pairwise details are retained in Q3C_multiscale_stability.csv.
7. zero/missing main-modality disagreement: 37.363%.
8. Modality audit: T: n=573, mean faithfulness=0.547; A: n=33, mean faithfulness=0.136; V: n=122, mean faithfulness=0.409. All modalities are finite and complete. Audio has distinctly weaker faithfulness under both baselines; Vision is especially weak under missing. Text dominates and has the explicit missing-OOD caveat. Detailed true-class/agreement groups are in Q3C_subgroup_audit.csv; groups n<30 are descriptive only.
9. R2-MISSING Text risk: present and material. Synthetic text-missing was outside R2 training distribution; missing selects Text for most samples, so every such row is marked TEXT_MISSING_OOD_CAUTION and is not treated as clean evidence that missing is the better semantic baseline.
10. Attachment4 next stage: allowed; Q3D was not run.

## Contract note

All attribution uses the fixed clean class and un-clipped affine regression value. Attention/gating weights are not treated as contribution truth.
