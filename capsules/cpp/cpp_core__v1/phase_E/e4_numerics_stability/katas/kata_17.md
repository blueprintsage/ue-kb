---
title: E4/k17 — Adaptive Step (RKF45-lite)
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Implement a simple embedded Runge–Kutta step with error control.
## Task
Use RK4 and a cheaper 3rd-order estimate to get local error; adapt dt to meet tolerance.
## Acceptance
- [ ] Error per step ≤ tol while minimizing steps on test ODE.
- [ ] No infinite step-halving loops; min/max dt respected.
## Keep/Revert
KEEP: reject/redo step on error>tol. REVERT: accept all steps regardless of error.