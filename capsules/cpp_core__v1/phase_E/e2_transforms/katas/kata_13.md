---
title: E2/k13 — Extract Scale & Shear
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
From a 3×3 affine basis, compute non‑uniform scales and XY/XZ/YZ shears.
## Task
QR‑like approach or Gram–Schmidt to get orthonormal axes, then read scales; compute shear from dot products.
## Acceptance
- [ ] Recompose TRS' matches original within 1e‑5.
- [ ] Negative scale cases handled with handedness fix.
## Keep/Revert
KEEP: track sign to keep det>0 in R. REVERT: ignore negative scale.