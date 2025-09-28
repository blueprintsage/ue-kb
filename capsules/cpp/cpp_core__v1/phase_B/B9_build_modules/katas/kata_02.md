---
title: B9/k2 — Producer/consumer with condition_variable
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Implement a bounded queue with `mutex` + `condition_variable`.
## Acceptance
- [ ] No lost/duplicated items across N producers/consumers; clean shutdown.
