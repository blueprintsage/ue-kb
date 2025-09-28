---
title: F4/k9 — UCT (Upper Confidence Bounds for Trees)
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Add **UCT** selection: `argmax(Q_i + c * sqrt(ln N / n_i))`.
## Task
Tune exploration c; handle unvisited children with +∞ policy or prior.
## Acceptance
- [ ] Balanced exploration/exploitation; improved win rate vs greedy.
- [ ] No divide‑by‑zero; numerics stable.