---
title: E3/k7 — Sphere–Sphere Time of Impact (Linear)
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Compute first contact time between two spheres moving linearly.
## Task
Reduce to ray-sphere: relative motion v, origin at center difference; solve quadratic for t where ‖o+tv‖=r1+r2.
## Acceptance
- [ ] Correct t for pass-through, grazing (discriminant≈0), and miss.
- [ ] Negative t ignored (past collisions) by policy.
## Keep/Revert
KEEP: discriminant clamp to 0. REVERT: take larger root unconditionally.