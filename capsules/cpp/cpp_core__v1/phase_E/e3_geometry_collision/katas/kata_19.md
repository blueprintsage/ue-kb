---
title: E3/k19 — GJK Collision (Convex–Convex)
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Detect intersection between two convex shapes using the **GJK** algorithm.
## Task
Implement support mappings and simplex evolution (2,3,4-simplex); return In/Out.
## Acceptance
- [ ] Correct on boxes/spheres/capsules; no false positives.
- [ ] Terminates within fixed iterations; epsilon guards.
## Keep/Revert
KEEP: robust simplex handling & tolerance. REVERT: unconstrained loop.