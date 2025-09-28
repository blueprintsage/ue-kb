---
title: E3/k10 — SAT 3D (OBB vs OBB)
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Perform 3D SAT overlap test for two oriented boxes using 15 axes.
## Task
Test axes: A’s 3, B’s 3, and 9 cross products. Compute projected radii and center distance per axis.
## Acceptance
- [ ] Agrees with OBB triangle-mesh intersection on randomized cases.
- [ ] Numerically stable with near-parallel axes.
## Keep/Revert
KEEP: epsilon on cross-product axes with tiny length. REVERT: unguarded division by tiny axes.