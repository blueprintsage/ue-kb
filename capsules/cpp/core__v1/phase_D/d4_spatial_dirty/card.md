---
title: D4 — Spatial Partition, Dirty Flag
kit_id: d4_spatial_dirty
version: 1.0
status: Draft
category: Patterns
assets: []
dependencies: [d1_update_loop_component]
---


## Objective
Speed up queries with a **Spatial Partition** (uniform grid or quadtree) and reduce recomputation with a **Dirty Flag** system that invalidates cached results on change.


## Steps
1) Uniform grid: bucket entities by cell; query neighbors within radius.
2) Quadtree (optional): insert, split, query; compare to grid for sparse data.
3) Dirty flags: cache AABB or expensive metric; mark dirty on mutation; recompute lazily.
4) Chain invalidation: dependent values recompute when inputs change.
5) Broad‑phase collision: use partition to filter candidate pairs.


## Smoke Test
- [ ] Grid query returns same set as naive within epsilon.
- [ ] Dirty flag avoids recompute when inputs stable.


## Blueprint Hook
**What transfers:** partition and cache; only recompute when inputs change.


## Keep/Revert
KEEP: uniform grid + dirty flags; REVERT: quadtree if time is short.