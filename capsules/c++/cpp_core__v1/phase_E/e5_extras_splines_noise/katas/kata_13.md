---
title: E5/k13 — Uniform Cubic B-Spline (Cox–de Boor)
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Evaluate a **uniform cubic B-spline** using Cox–de Boor and compare to de Boor’s algorithm.
## Task
Given control points and uniform knot vector, implement basis recursion; verify partition of unity and C2 continuity.
## Acceptance
- [ ] Basis sums to 1; derivatives are continuous at knots.
- [ ] Matches de Boor evaluation within 1e-6.
## Keep/Revert
KEEP: stable recursion with cached subresults. REVERT: recompute basis naively each sample.