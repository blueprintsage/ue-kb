---
title: E3/k21 — Triangle–Triangle Intersection (3D)
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Detect intersection between two 3D triangles with a robust coplanar fallback.
## Task
Implement Möller ’97 tri–tri test; when triangles are coplanar within ε, project to the dominant 2D plane and run 2D polygon overlap.
## Acceptance
- [ ] Matches brute-force mesh sampling on randomized pairs.
- [ ] Coplanar/edge-touch cases handled without flicker.
## Keep/Revert
KEEP: 2D projection for coplanar fallback. REVERT: rely on 3D tests only (unstable near-coplanar).