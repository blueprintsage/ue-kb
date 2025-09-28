---
title: F4/k17 — UCB1 & UCB‑Tuned Bandits
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Use **Upper Confidence Bounds** for principled exploration.
## Task
Implement UCB1: `Q_i + sqrt(2 ln t / n_i)` and UCB‑Tuned using variance estimate; compare cumulative regret vs ε‑greedy/softmax.
## Acceptance
- [ ] UCB variants show lower regret on canonical tests.
- [ ] Handles cold‑start (n_i=0) with +∞ or forced one‑try policy.