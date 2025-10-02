---
title: E3/k11 — Point↔AABB: Closest Point & Distance
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Compute closest point on an axis-aligned box to a query point and the squared distance.
## Task
Clamp each coordinate of p to [min,max] to get p*; return ‖p−p*‖².
## Acceptance
- [ ] Matches brute-force sampling on random boxes/points.
- [ ] Inside-box case returns distance 0 and p*=p.
## Keep/Revert
KEEP: clamp per axis. REVERT: project to center and clamp length.