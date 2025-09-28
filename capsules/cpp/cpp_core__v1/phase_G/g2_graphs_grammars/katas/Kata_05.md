---
title: G2/k5 — BSP Dungeon (Rooms & Corridors)
kit_id: g2_graphs_grammars
version: 1.0
status: Draft
type: kata
---
## Objective
Partition space using BSP, place rooms, connect with corridors.
## Tasks
- Recursively split with min room size; place rooms in leaves; connect sibling leaves by corridors (straight/L‑shaped).
## Acceptance
- [ ] All rooms connected; dead‑ends ≤ target ratio or culled.  
- [ ] Parameters produce varied yet valid layouts.