---
title: B9/k9 — Futures & packaged_task pipeline
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Chain async steps with futures, ensuring no deadlocks.
## Acceptance
- [ ] Pipeline completes with expected value; no blocking on same thread; TSan clean.
