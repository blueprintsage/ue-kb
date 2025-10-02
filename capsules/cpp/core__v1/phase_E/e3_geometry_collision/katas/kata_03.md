---
title: E3/k3 — Ray–AABB (Slab Method)
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Intersect a ray with an axis-aligned box using per-axis slabs.
## Task
For each axis, compute t1=(min−o)/d, t2=(max−o)/d; swap if needed; tmin=max(tmin,t1); tmax=min(tmax,t2). Hit if tmax≥max(0,tmin).
## Acceptance
- [ ] Agrees with reference implementation; handles negative/zero d components.
- [ ] Returns entry/exit t values with correct ordering.
## Keep/Revert
KEEP: reciprocal dir with infinity handling. REVERT: branching per sign without guards.