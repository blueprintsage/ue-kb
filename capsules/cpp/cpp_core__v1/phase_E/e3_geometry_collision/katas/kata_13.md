---
title: E3/k13 — Robust Ray–Sphere (Quadratic, Safe)
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Implement ray–sphere intersection that avoids catastrophic cancellation.
## Task
Use quadratic in terms of b = dot(m,d), c = dot(m,m) − r² with m=o−c; compute q=−b±√(b²−c) choosing sign by b; t0 = q, t1 = c/q.
## Acceptance
- [ ] Matches naive solution but remains stable for grazing hits.
- [ ] Correctly handles rays starting inside sphere.
## Keep/Revert
KEEP: stable quadratic form. REVERT: direct formula for t causing precision loss.