---
title: F2/k10 — Preemption & Resume (Pushdown Stack)
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Handle interrupts (e.g., dodge) by pausing current task and resuming after.
## Task
Push interrupted task onto a stack; run interrupt; pop and resume with saved context.
## Acceptance
- [ ] No lost state; resume produces same result as continuous run.
- [ ] Max stack depth bounded; overflow handled.