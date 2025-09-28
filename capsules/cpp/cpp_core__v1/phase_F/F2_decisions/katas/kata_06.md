---
title: F2/k6 — BT Decorators (Cooldown, Inverter, TimeLimit)
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Add common decorators and verify semantics.
## Task
Wrap actions with Cooldown, Inverter, Succeeder, and TimeLimit; write table tests.
## Acceptance
- [ ] Cooldown suppresses re-entry; TimeLimit turns Running→Failure.
- [ ] Inverter/Succeeder flip as expected.