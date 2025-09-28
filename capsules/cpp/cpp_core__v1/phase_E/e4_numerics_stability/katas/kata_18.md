---
title: E4/k18 — Gradient Descent Step Size (Convex Quadric)
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Show stability bounds for gradient descent on f(x)=0.5 x^T Q x with Q SPD.
## Task
Compute largest eigenvalue λ_max(Q) (power iteration); stable α∈(0,2/λ_max). Verify convergence/divergence empirically.
## Acceptance
- [ ] Converges for α below bound; diverges above.
- [ ] Rate matches (1−αλ_min) per-iteration envelope.
## Keep/Revert
KEEP: estimate λ_max first. REVERT: arbitrary α selection.