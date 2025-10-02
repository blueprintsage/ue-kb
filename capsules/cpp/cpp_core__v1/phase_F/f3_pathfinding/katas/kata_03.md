---
title: F3/k3 — Dijkstra vs A* (Parity at h=0)
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Show that A* reduces to Dijkstra when heuristic h=0 and matches path costs.
## Task
Run both on random maps; compare expansions and path costs.
## Acceptance
- [ ] Costs identical; A* expansions ≤ Dijkstra when h>0.
- [ ] With h=0, expansions equal within ±1%.