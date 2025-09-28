---
title: E3/k1 — Ray–Plane Intersection
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Compute intersection point of a ray with a plane and handle parallel cases robustly.
## Task
Ray r(t)=o+td, plane n·x=d0 with unit n. Solve t=(d0−n·o)/(n·d). If |n·d|<ε → no hit/parallel.
## Acceptance
- [ ] For non-parallel, point p=o+td satisfies |n·p−d0|<1e−6.
- [ ] Parallel rays return no hit or t=∞ by policy.
## Keep/Revert
KEEP: epsilon on denominator; unit-normalize n. REVERT: divide by ~0.