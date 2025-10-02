---
title: G2/k8 — Poisson Disk Room Placement
kit_id: g2_graphs_grammars
version: 1.0
status: Draft
type: kata
---
## Objective
Place rooms with Bridson’s Poisson disk sampling and ensure min spacing.
## Tasks
- Implement 2D sampler with active list/grid; reject samples closer than r; seedable.
## Acceptance
- [ ] No overlaps; min gap respected; O(n).  
- [ ] Seeds reproduce placements.