---
title: E3/k18 — Tiny BVH: Build & Ray Query
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Build a minimal binary BVH over triangles (median split) and implement a ray traversal.
## Task
Compute AABBs, recursive split by longest axis median; depth-first ray test; return first hit.
## Acceptance
- [ ] Speedup vs brute-force on ≥1k tris.
- [ ] Correct hits identical to brute-force results.
## Keep/Revert
KEEP: order children by entry t for early-out. REVERT: always visit both without ordering.