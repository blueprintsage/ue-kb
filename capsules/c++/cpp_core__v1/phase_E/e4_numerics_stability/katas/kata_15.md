---
title: E4/k15 — Condition Number Estimate
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Estimate κ₂(A) ≈ ‖A‖₂ ‖A^{-1}‖₂ for 3×3 using power iteration on A^T A.
## Task
Compute largest singular value via power iteration; smallest via inverse iteration (or estimate via reciprocal on (A^{-1})^T (A^{-1})).
## Acceptance
- [ ] Estimates within 5% of SVD on random matrices.
- [ ] Flag ill-conditioned when κ₂ > 1e6.
## Keep/Revert
KEEP: normalize each iteration. REVERT: unnormalized iterations (diverge).