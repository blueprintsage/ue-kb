---
title: G2 — Graphs & Grammars
kit_id: g2_graphs_grammars
version: 1.0
status: Draft
category: PCG
assets: []
dependencies: []
---

## Objective
Build level generators using graph/grammar techniques: L‑systems, WFC, BSP/cellular automata, room graphs, and CFG macro‑layout.

## Steps
1) **Strings→Geometry:** L‑system rewrite → turtle draw; add stochastic/context rules.  
2) **Constraints:** Wave Function Collapse with backtracking and masks.  
3) **Space partition:** BSP rooms/corridors; CA caves; random‑walk carvers.  
4) **Graphs:** room placement (Poisson disk), MST connectivity, A* corridor routing.  
5) **Meta:** tagging/theming, seeding & reproducibility.

## Smoke Test
- [ ] Outputs are connected; constraints never violated (WFC).  
- [ ] Seeds reproduce layouts; metrics (coverage/branching) within bands.