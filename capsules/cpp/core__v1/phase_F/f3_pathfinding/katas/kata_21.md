---
title: F3/k21 — Landmarks Heuristic (ALT)
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Speed up A* using the **ALT** heuristic: A* with triangle‑inequality lower bounds from precomputed **A**ll‑pairs to **L**andmarks and **T**riangle inequality.
## Task
Pick K landmarks; precompute distances d(L↔V). Heuristic h(u,v)=max_L |d(L,v)−d(L,u)| (and/or |d(u,L)−d(v,L)|). Integrate into A*.
## Acceptance
- [ ] Heuristic is admissible/consistent; A* remains optimal.
- [ ] Node expansions drop vs Octile/Manhattan on large maps; report speedup.