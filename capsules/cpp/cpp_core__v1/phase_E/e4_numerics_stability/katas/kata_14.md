---
title: E4/k14 — 3×3 Solve (GE with Partial Pivoting)
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Solve A x = b robustly using Gaussian elimination with **partial pivoting**.
## Task
Implement GEPP for 3×3; compare to inverse(A)*b and to Eigen/blas reference if available.
## Acceptance
- [ ] Residual ‖A x − b‖ < 1e-10 on random well-conditioned systems.
- [ ] Handles near-singular with detect+report (condition estimate).
## Keep/Revert
KEEP: row swaps on max pivot. REVERT: no pivoting.