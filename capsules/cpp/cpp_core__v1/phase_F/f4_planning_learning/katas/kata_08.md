---
title: F4/k8 — MCTS Core (Selection/Expansion/Rollout/Backprop)
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Implement **MCTS** skeleton with pluggable game/environment interface.
## Task
Define Node with visit count/value; selection by UCT; expand one child; simulate with random/heuristic policy; backprop returns.
## Acceptance
- [ ] Value estimates converge with more iterations.
- [ ] Deterministic with fixed RNG seed.