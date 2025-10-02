---
title: F3/k13 — Lifelong Planning A* (LPA*)
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Implement **LPA*** core update equations for changing edge costs.
## Task
Maintain g/rhs per node; use priority by min(g,rhs)+h; update affected nodes after cost changes.
## Acceptance
- [ ] Identical path to fresh A* after changes; fewer expansions.
- [ ] Correctness under multiple sequential updates.