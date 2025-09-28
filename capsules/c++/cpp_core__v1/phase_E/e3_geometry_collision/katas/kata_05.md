---
title: E3/k5 — Segment–Segment Closest Points (3D)
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Compute closest points between two finite 3D segments and their distance.
## Task
Solve for parameters s,t on [0,1] minimizing ‖(p0+s*u)−(q0+t*v)‖; clamp to segment bounds.
## Acceptance
- [ ] Matches analytical cases (parallel, skew, intersecting).
- [ ] Symmetry: swapping segments yields same distance.
## Keep/Revert
KEEP: handle near-parallel with fallback. REVERT: unclamped infinite-line solution.