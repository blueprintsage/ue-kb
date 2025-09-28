---
title: F4/k10 — Rollout Policies & Heuristic Bias
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Improve MCTS by using simple heuristic rollouts instead of purely random.
## Task
Plug in a domain heuristic (e.g., prefer cover, avoid hazards); compare convergence speed and final reward vs random rollouts.
## Acceptance
- [ ] Faster convergence to good actions (fewer iterations to target win rate).
- [ ] No bias collapse (still explores alternatives under UCT).