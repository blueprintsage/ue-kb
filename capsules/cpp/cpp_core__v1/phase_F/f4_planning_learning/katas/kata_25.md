---
title: F4/k25 — Planning & Learning Harness (Parity/Regret)
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Benchmark GOAP, MCTS, and bandits end‑to‑end on canonical scenarios; report **parity** and **regret**.
## Task
Run fixed‑seed suites; collect: time‑to‑goal, cost, success rate, cumulative regret (bandits). Export CSV + plot; choose defaults by evidence.
## Acceptance
- [ ] Zero invariant failures; seeds logged for worst cases.
- [ ] Clear winner per scenario; recommended defaults recorded in card.
## Keep/Revert
KEEP: reproducible seeds + CSV outputs. REVERT: eyeball comparisons only.