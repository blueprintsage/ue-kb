---
title: F3/k18 — Grid→Navmesh Bridge (Funnel Setup)
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Convert a grid path into a portal sequence suitable for **funnel** smoothing.
## Task
Identify wall crossings between cells; produce alternating left/right portal points; validate ordering.
## Acceptance
- [ ] Funnel input valid (no self‑intersections); portal count reduced vs cells.
- [ ] Resulting smoothed path is collision‑free.