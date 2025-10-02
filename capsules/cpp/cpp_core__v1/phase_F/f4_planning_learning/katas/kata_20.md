---
title: F4/k20 — Bandits Harness: Regret & Convergence Plots
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Create a test harness to compare bandit algorithms on synthetic tasks.
## Task
Run ε‑greedy, softmax, UCB1, UCB‑Tuned, Thompson on stationary and drifting rewards; record cumulative regret, action frequencies; export CSV.
## Acceptance
- [ ] Plots/regret tables show expected rankings; seeds logged for repro.
- [ ] Zero crashes/NaNs across 10k trial runs.