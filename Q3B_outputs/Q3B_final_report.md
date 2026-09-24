# Q3B Frozen Final-Q2 Reproduction & Coalition Audit

- Decision: **PASS_BOTH_FEASIBLE_NEEDS_Q3C**
- Frozen model: Q2D-R2-AV-MultiGap + Global Affine Calibration
- Formal calibration: `y = clip(0.8 * y_raw + 0.009049484133720337, -3, 3)`

## Reproduction gate

- PASS: True
- valid: class exact=True, raw max error=7.65e-17, metric max error=9.48e-09
- test: class exact=True, raw max error=8.76e-17, metric max error=4.3e-08

## Coalition audit

- zero: finite=1.000000, Shapley residual(cls/reg)=8.88e-16/4.44e-16, ranks(cls/reg)=T>V>A/T>V>A
- missing: finite=1.000000, Shapley residual(cls/reg)=1.78e-15/8.88e-16, ranks(cls/reg)=T>A>V/T>V>A

## Interpretation

NEUTRAL-ZERO measures input-information contribution in the frozen model input space. R2-MISSING measures sensitivity to a modality-unavailable state; its missing-token/compensator effect is not itself evidence of modality information.
Zero-feature audit cases: 17; neutral-zero idempotence all pass: True.
