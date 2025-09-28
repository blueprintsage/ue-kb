---
title: F4/k16 — ε‑Greedy & Softmax Bandits (Annealing)
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Implement **ε‑greedy** and **softmax/Boltzmann** action selection with optional annealing schedules.
## Task
Update action value estimates via sample mean; pick action via ε or softmax(τ). Anneal ε↓ and τ↓ over time; log regret.
## Acceptance
- [ ] Converges to best arm on stationary rewards; regret decreases over time.
- [ ] Annealing improves exploitation without early lock‑in.