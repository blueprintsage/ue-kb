---
title: E5/k22 — Arc-Length Reparameterization (Newton Refine)
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Map desired arc distance s to parameter t for a cubic (Bezier/Hermite) using Newton iteration on length(t).
## Task
Start from LUT guess (E5/k5), iterate t_{k+1} = t_k − (L(t_k)−s)/‖p'(t_k)‖ with clamp to [0,1]; stop at tolerance.
## Acceptance
- [ ] ≤3 iterations average to reach |Δs|<1e−4 of total length.
- [ ] Monotone mapping s↦t; no overshoot at boundaries.
## Keep/Revert
KEEP: seed from coarse LUT; cap iterations & step size. REVERT: raw Newton from t= s.**