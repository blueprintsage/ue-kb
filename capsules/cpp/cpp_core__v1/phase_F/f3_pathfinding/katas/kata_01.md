---
title: F3/k1 — Grid Graph Build (4/8‑Connectivity)
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Construct a tile grid with obstacles, movement costs, and 4/8‑connectivity toggles.
## Task
Input occupancy/cost map; build adjacency with cost 1 (orthogonal) and √2 (diagonal, if enabled); block corner‑cutting policy.
## Acceptance
- [ ] Adjacency count per tile matches mode (4 or 8).
- [ ] No diagonal through "forbidden corner" when either adjacent is blocked.