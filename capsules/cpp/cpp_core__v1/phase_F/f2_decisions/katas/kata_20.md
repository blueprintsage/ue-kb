---
title: F2/k20 — Cross‑Framework Parity Test (FSM vs BT vs Utility)
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Validate that FSM, BT, and Utility solve a canonical scenario with comparable outcomes and latencies.
## Task
Define a scenario (patrol→chase→search with hazards). Implement in all three and compare time‑to‑catch and path length.
## Acceptance
- [ ] Metrics within ±10% across frameworks (given same inputs).
- [ ] Deterministic replay reproduces parity metrics exactly.