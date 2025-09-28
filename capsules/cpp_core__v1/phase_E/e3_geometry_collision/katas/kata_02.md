---
title: E3/k2 — Ray–Triangle (Möller–Trumbore)
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Implement Möller–Trumbore to test a ray against a triangle with barycentric outputs.
## Task
Given (A,B,C), compute t,u,v; hit if u∈[0,1], v∈[0,1], u+v≤1, t≥0.
## Acceptance
- [ ] Matches brute-force plane+inside test on random cases.
- [ ] Backface culling optional toggle; epsilon guards on det.
## Keep/Revert
KEEP: det threshold; return barycentrics. REVERT: naive 2D projection test.