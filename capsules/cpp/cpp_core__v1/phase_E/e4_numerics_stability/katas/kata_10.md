---
title: E4/k10 — Finite-Difference Gradient Check
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Verify analytic gradients against numerical finite differences.
## Task
Pick a smooth f(x): R^n→R (e.g., quadratic + sinusoid). Compute analytic ∇f and compare to central-difference approximation with step h.
## Acceptance
- [ ] Error scales ~O(h^2) as h shrinks until roundoff dominates.
- [ ] Choose optimal h ~ √ε |x|; document when errors rise.
## Keep/Revert
KEEP: central difference; vary h to see error curve. REVERT: forward difference only.