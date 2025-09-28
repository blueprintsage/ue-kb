---
title: F1/k10 — Time‑Sliced Queries & Budget
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Throttle expensive perception/path queries across frames to meet a budget.
## Task
Distribute N agents’ heavy checks round‑robin; ensure per‑frame cost ≤ budget while behavior remains responsive.
## Acceptance
- [ ] Frame time within target; max query latency bounded.
- [ ] Identical decisions vs naive all‑every‑frame baseline within tolerance.