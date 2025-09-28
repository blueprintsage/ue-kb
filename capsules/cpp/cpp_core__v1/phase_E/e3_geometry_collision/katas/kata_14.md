---
title: E3/k14 — Capsule–Sphere Contact
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Compute distance/overlap between a capsule (segment + radius R) and a sphere (center, radius r).
## Task
Closest point from sphere center to capsule segment; compare distance to R+r; return penetration/outside info.
## Acceptance
- [ ] Matches analytical edge cases (touching ends/sides).
- [ ] Robust for near-parallel segment/sphere-center alignment.
## Keep/Revert
KEEP: segment clamp of parameter t∈[0,1]. REVERT: use infinite line distance.