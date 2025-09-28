---
title: F2/k11 — BT Services & Tick Intervals
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Run periodic sensing/evaluation via **services** attached to subtrees; control rates to meet budget.
## Task
Add a service to a Selector that refreshes blackboard keys (LOS/FOV) every N frames; stagger per‑agent phases to avoid spikes.
## Acceptance
- [ ] Average CPU ≤ budget; no frame spikes > 2× budget.
- [ ] Blackboard freshness ≤ N frames; decisions unaffected vs per‑frame baseline within tolerance.