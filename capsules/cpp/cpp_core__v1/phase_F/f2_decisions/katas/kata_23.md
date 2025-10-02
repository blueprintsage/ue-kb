---
title: F2/k23 — Global Interrupt Priorities (BT + FSM)
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Route high‑priority interrupts (e.g., dodge) through a **global arbiter** that can preempt BT/FSM work safely.
## Task
Maintain a priority queue of interrupts; when raised, pushdown current task (F2/k10) and run interrupt; resume on completion.
## Acceptance
- [ ] No lost/corrupted state after nested interrupts.
- [ ] Measured preemption latency ≤ 1 tick.
## Keep/Revert
KEEP: single arbiter + priorities; idempotent handlers. REVERT: each subsystem preempts independently.