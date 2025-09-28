---
title: E2/k23 — Best‑Fit Rotation (Kabsch/Procrustes)
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Find rotation `R` that best aligns two point sets `{a_i}`→`{b_i}` in least squares.
## Task
Center both sets, compute covariance `H = A^T B`, SVD `H = U Σ V^T`, set `R = V diag(1,1,det(VU^T)) U^T`. Compare RMS error.
## Acceptance
- [ ] `R` is orthonormal with det=+1.
- [ ] RMS error minimized vs a random rotation baseline.
## Keep/Revert
KEEP: reflection fix via determinant sign. REVERT: `R = VU^T` without det correction.