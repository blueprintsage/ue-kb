---
title: F4/k3 — GOAP Planner via A* on State Space
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Search from initial state to any goal‑satisfying state using A* over actions.
## Task
Nodes are states; edges are applicable actions; reconstruct action sequence; track visited with hash.
## Acceptance
- [ ] Finds minimal‑cost plan if heuristic admissible; equals Dijkstra at h=0.
- [ ] Detects unsolvable goals (frontier exhausted).