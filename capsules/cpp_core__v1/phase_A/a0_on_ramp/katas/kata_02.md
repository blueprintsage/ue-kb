---
title: A0/k2 — lifetime trace
kit_id: a0_on_ramp
version: 1.0
status: Draft
type: kata
---
## Goal
Observe construction/destruction order for stack vs heap.
## Task
Instrument a small type with counters and scope blocks.
## Acceptance
- [ ] Counts show deterministic destroy on scope exit.
- [ ] Heap instance destroyed by RAII owner.