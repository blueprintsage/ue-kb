---
title: E3/k20 — EPA Penetration Depth (post-GJK)
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
When GJK reports intersection, compute penetration depth and contact normal using **EPA**.
## Task
Expand polytope from GJK simplex; iteratively push along closest face normal until convergence.
## Acceptance
- [ ] Depth/normal matches analytic cases (sphere-sphere, box-plane).
- [ ] Converges in bounded iterations with epsilon tolerance.
## Keep/Revert
KEEP: heap of faces by distance; handle degenerate faces. REVERT: arbitrary face selection.