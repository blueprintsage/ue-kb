---
title: E5/k5 — Arc-Length Approximation
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Approximate curve length and build a lookup for approximately uniform parameterization by distance.
## Task
Sample N points along curve; sum segment lengths (piecewise linear). Build cumulative table and invert via binary search.
## Acceptance
- [ ] Length within 1% of fine-sampled ground truth for N≥64.
- [ ] Inverse table maps equal arc steps to ≈equal t steps (max error reported).
## Keep/Revert
KEEP: adaptive subdivision where curvature high. REVERT: fixed coarse N on sharp curves.