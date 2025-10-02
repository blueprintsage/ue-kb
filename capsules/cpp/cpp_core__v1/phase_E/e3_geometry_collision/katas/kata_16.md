---
title: E3/k16 — Triangle–AABB Overlap (SAT Variant)
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Test if a triangle intersects an axis-aligned box using SAT (13 axes test).
## Task
Test axes: box axes (3), triangle normal (1), and 9 cross products of box axes with triangle edges.
## Acceptance
- [ ] Matches reference implementation across random poses.
- [ ] Stable for nearly coplanar/edge-touching cases.
## Keep/Revert
KEEP: epsilon for tiny axes and projections. REVERT: omit cross-product axes.