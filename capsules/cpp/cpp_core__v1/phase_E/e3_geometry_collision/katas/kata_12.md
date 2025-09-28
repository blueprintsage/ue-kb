---
title: E3/k12 — Closest Point on OBB to Point
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Find the closest point on an oriented box to p using box-local coordinates.
## Task
Transform p into box space with R^T; clamp to half-extents; transform back.
## Acceptance
- [ ] Symmetry test vs analytic cases; zero when inside.
- [ ] Stable with slightly non-orthonormal axes (re-orthonormalize).
## Keep/Revert
KEEP: re-ONB axes; clamp in local space. REVERT: clamp in world space.