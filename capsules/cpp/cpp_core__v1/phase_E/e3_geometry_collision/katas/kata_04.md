---
title: E3/k4 — Ray–OBB via Box Space
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Test a ray against an oriented box by transforming into box-local space.
## Task
Given OBB {center, axes, half-extents}, transform ray to box space with R^T; use AABB slab test.
## Acceptance
- [ ] Results match brute-force triangle-mesh box on random OBBs.
- [ ] Numerical stability within 1e−6.
## Keep/Revert
KEEP: orthonormalize axes before invert. REVERT: invert 3×3 without checking.