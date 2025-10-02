---
title: B9/k4 — Atomic counter: relaxed vs seq_cst
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Compare correctness/ordering using `memory_order_relaxed` vs `seq_cst`.
## Acceptance
- [ ] Litmus test shows where relaxed is safe; seq_cst variant always correct; TSan clean.
