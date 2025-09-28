---
title: F3/k6 — Tie‑Breaking & Turn Cost
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Reduce stair‑step paths by favoring straight movement or penalizing turns.
## Task
Augment g with small turn penalty or prefer higher g on equal f; compare path smoothness.
## Acceptance
- [ ] Fewer direction changes with minimal cost inflation.
- [ ] No loss of optimality under consistent tie‑break.