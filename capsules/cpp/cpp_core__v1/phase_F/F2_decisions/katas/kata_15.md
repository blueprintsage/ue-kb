---
title: F2/k15 — Action Queue & Cancellation Semantics
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Manage a small **command queue** for actions emitted by BT/Utility; define cancellation priorities.
## Task
Queue supports push/pop/cancel‑by‑tag; preemption inserts high‑priority action at head; log transitions.
## Acceptance
- [ ] No dangling actions after cancel; invariants maintained.
- [ ] High‑priority inserts preempt within ≤1 frame.