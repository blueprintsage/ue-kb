---
title: F4/k15 — MCTS Budgets & Termination (Time/Rollouts)
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Terminate search predictably under real‑time constraints (e.g., 2 ms per tick).
## Task
Support stop by wall‑clock, by iterations, or by leaf expansions; keep running stats to allocate per‑agent budgets fairly.
## Acceptance
- [ ] Budget respected within ±5%; best child stable across repeats.
- [ ] Deterministic choice under fixed seed and identical timing.