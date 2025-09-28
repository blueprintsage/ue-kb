---
title: E5/k17 — Perlin Gradient & Flow Field
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Compute analytical gradient of 2D Perlin noise and use it to build a divergence-free flow field.
## Task
Differentiate fade and dot with lattice gradients; define velocity field v = (∂y n, −∂x n).
## Acceptance
- [ ] Numeric gradient (finite diff) matches analytic within tolerance.
- [ ] Flow field shows closed streamlines; ∇·v≈0 numerically.
## Keep/Revert
KEEP: reuse hashed gradients for gradient eval. REVERT: new RNG per gradient call.