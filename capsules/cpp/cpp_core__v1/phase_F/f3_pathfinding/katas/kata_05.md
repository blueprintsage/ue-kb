---
title: F3/k5 — Weighted A* (ε‑Suboptimal)
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Trade optimality for speed using f = g + w·h with w≥1.
## Task
Run series over w∈{1,1.2,1.5,2}; report expansions and cost ratio vs optimal.
## Acceptance
- [ ] Cost ≤ w×optimal; expansions drop as w grows.
- [ ] Reverts to optimal as w→1.