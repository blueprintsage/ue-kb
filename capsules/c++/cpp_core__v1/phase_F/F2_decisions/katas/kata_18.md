---
title: F2/k18 — Hybrid Orchestration: FSM ↔ BT/Utility
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Use **FSM** to gate high‑level modes (combat/search/idle) and run BT/Utility inside modes.
## Task
Superstate selects subtree or utility slate; on state change, cancel running tasks and clear scoped blackboard keys.
## Acceptance
- [ ] No cross‑mode leaks; transitions deterministic.
- [ ] Latent actions terminate cleanly on mode switch.