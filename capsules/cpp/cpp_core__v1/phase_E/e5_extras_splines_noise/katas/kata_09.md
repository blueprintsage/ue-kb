---
title: E5/k9 — Domain Warp (Flow Noise)
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Perturb input coordinates by another noise field to create warped patterns.
## Task
Compute d = noise2(x,y); output = base_noise(x + k*d.x, y + k*d.y); choose k scale; visualize.
## Acceptance
- [ ] Warping increases apparent complexity without aliasing.
- [ ] No discontinuities; sample continuity preserved.
## Keep/Revert
KEEP: low-frequency warp field. REVERT: warp at same frequency as base (aliasy patterns).