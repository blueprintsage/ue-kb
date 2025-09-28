---
title: E3/k9 — SAT 2D (Convex Polygons)
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Implement Separating Axis Theorem overlap test for two 2D convex polygons.
## Task
Test projections on all unique edge normals; track minimum penetration and axis.
## Acceptance
- [ ] Matches reference poly pairs; reports separating axis when disjoint.
- [ ] Returns contact normal pointing from A to B.
## Keep/Revert
KEEP: cache edge normals; consistent winding. REVERT: test only A’s axes.