---
title: G2/k9 — Connectivity: MST & Corridor Routing
kit_id: g2_graphs_grammars
version: 1.0
status: Draft
type: kata
---
## Objective
Connect rooms via a minimum spanning tree, then route corridors on a grid.
## Tasks
- Build room graph weighted by distance; MST via Kruskal/Prim; route corridors with A* respecting widths and walls.
## Acceptance
- [ ] All rooms connected; optional extra edges for loops ≤ target.  
- [ ] Corridor widths respected; no illegal diagonals.