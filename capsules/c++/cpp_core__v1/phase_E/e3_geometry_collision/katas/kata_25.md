---
title: E3/k25 — Geometry Fuzz/Property Harness
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Property-test the geometry library across randomized scenes; assert invariants and cross-check algorithms.
## Task
Generate random rays/boxes/triangles; assert symmetry where applicable, conservation (e.g., closest(A,B)=closest(B,A)), and cross-validate ray–mesh vs BVH.
## Acceptance
- [ ] 10k trials with zero assertion failures; logs capture min/max epsilons.
- [ ] Sanitizers clean; time budget < X ms.
## Keep/Revert
KEEP: seeded RNG + reproducible failures. REVERT: purely random with no seed/logs.