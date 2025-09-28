---
title: E2/k4 — Fast Inverse (Rigid Transform)
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Invert a rigid transform (no scale) using transpose rotation and translated origin.
## Task
Given R (orthonormal) and t, compute R^T and t' = −R^T t; compare to general 4×4 inverse.
## Acceptance
- [ ] Results match general inverse within 1e‑6.
- [ ] Reject when scale/shear present.
## Keep/Revert
KEEP: assert orthonormality before fast path. REVERT: use fast inverse on scaled matrices.