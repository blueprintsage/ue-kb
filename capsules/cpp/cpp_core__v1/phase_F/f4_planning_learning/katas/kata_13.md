---
title: F4/k13 — RAVE/AMAF Heuristics (Shared Action Values)
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Speed early learning by blending node‑local Q with **RAVE/AMAF** action estimates.
## Task
Maintain Q_node and Q_rave; use β(n)=n/(n+k) to blend: Q'=(1−β)Q_node+β Q_rave; decay AMAF counts with depth.
## Acceptance
- [ ] Early‑game accuracy improves (fewer iterations to stable choice).
- [ ] Blending weight decays as visits grow; final policy ≈ vanilla UCT.