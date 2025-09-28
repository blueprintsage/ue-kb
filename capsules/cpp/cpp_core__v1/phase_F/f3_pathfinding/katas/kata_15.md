---
title: F3/k15 — HPA* (Clusters & Portals)
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Build **Hierarchical Path‑Finding A***: cluster grid into regions, compute portal graph, and plan at two levels.
## Task
Partition grid; compute intra‑cluster paths and inter‑cluster portal links; assemble high‑level path then refine.
## Acceptance
- [ ] Path within small factor of optimal; expansions drop substantially.
- [ ] Precompute time reasonable; cache reused across queries.