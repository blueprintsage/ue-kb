---
title: F3/k16 — Subgoal Graphs (Any‑Angle Speed‑up)
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Construct **subgoal graphs** from grid obstacles to speed any‑angle search.
## Task
Identify corners as subgoals; connect visible pairs; run A* over sparse graph; compare to Theta* on full grid.
## Acceptance
- [ ] Similar path length to Theta* with fewer expansions.
- [ ] Graph stays sparse; build cost acceptable.