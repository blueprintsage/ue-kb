---
title: E3 — Geometry & Collision
kit_id: e3_geometry_collision
version: 1.0
status: Draft
category: Math
assets: []
dependencies: [e1_vectors_spaces, e2_transforms]
---

## Objective
Implement core geometric queries: ray/segment tests, AABB/OBB, planes, SAT (2D/3D), closest points, and broad‑phase culling.

## Steps
1) Ray–plane/triangle; segment–segment distance.  
2) Ray–AABB/OBB; slab method.  
3) SAT overlaps (2D polygons, 3D boxes).  
4) Closest point on triangle/box/sphere.  
5) Broad‑phase culling with grid or BVH.

## Smoke Test
- [ ] All queries match analytical references within epsilon.  
- [ ] No NaNs for degenerate inputs (guarded).

## Blueprint Hook
BP: use line traces + simple SAT for 2D UI/gameplay; Acceptance: highlight only colliding items.