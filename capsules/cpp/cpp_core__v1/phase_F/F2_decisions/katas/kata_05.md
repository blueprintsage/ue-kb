---
title: F2/k5 — BT Primitives (Sequence, Selector, Action, Condition)
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Build a minimal Behavior Tree runtime.
## Task
Implement tick() with node statuses {Running, Success, Failure}; add Sequence, Selector, leaf Action/Condition.
## Acceptance
- [ ] Tree results match hand-evaluated traces.
- [ ] Running nodes resume correctly next tick.