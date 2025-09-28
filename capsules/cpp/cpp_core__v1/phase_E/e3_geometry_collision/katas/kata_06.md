---
title: E3/k6 — Closest Point on Triangle
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Return the closest point on a triangle to a query point using region tests.
## Task
Implement Voronoi-region checks (vertices, edges, face) per Ericson; return closest point and barycentrics.
## Acceptance
- [ ] Matches brute-force sampled minimization within 1e−6.
- [ ] Stable at edges/vertices with epsilon slop.
## Keep/Revert
KEEP: region order and clamp logic. REVERT: project to plane only.