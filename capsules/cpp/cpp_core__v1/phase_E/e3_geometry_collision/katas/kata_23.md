---
title: E3/k23 — Swept Sphere vs Triangle (CCD)
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Compute time of impact (first contact) between a moving sphere and a static triangle.
## Task
Test against tri plane (expanded by radius), then edges/vertices via capsule/point sweeps; choose earliest non-negative t.
## Acceptance
- [ ] Correct TOI for face, edge, and vertex hits (including grazing).
- [ ] No tunneling for dt under chosen bound in randomized trials.
## Keep/Revert
KEEP: check plane, then edges, then vertices. REVERT: plane-only test (misses edges/verts).