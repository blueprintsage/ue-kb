---
title: F2/k24 — Meta‑Controller: Framework Selection
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Pick **FSM vs BT vs Utility** per situation using a light meta‑policy (e.g., uncertainty, budget, number of options).
## Task
Define features (option count, variance of scores, time budget). If options few & clear → FSM/BT; if many/noisy → Utility. Log switch decisions.
## Acceptance
- [ ] Scenario metrics improve (latency or success) vs single‑framework baseline.
- [ ] No oscillation between frameworks (hysteresis).
## Keep/Revert
KEEP: hysteresis + min dwell time. REVERT: switch per‑tick on small deltas.