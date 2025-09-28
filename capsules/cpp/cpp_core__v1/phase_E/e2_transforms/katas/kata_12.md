---
title: E2/k12 — Polar Decomposition (A = R·S)
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Split an affine 3×3 A into rotation R and symmetric stretch S.
## Task
Use iterative `R_{k+1} = 0.5(R_k + (R_k^{-1})^T)` starting from A; set S = R^T A.
## Acceptance
- [ ] R orthonormal within 1e‑6; S symmetric (‖S−S^T‖ small).
- [ ] R·S approximates A within 1e‑5.
## Keep/Revert
KEEP: stop when change < ε. REVERT: single iteration only.