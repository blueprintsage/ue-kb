---
title: B9/k22 — Contended vs sharded counters
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Compare a single atomic counter to sharded counters with merge.
## Acceptance
- [ ] Sharded approach scales better under N threads; correctness of totals verified.
