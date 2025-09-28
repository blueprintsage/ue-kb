---
title: C3/k8 — concurrent_unordered_set
kit_id: c3_containers_allocators
version: 1.0
status: Draft
type: kata
---
## Goal
Concurrent insert/erase with final membership check.
## Task
Random ops from threads; assert final elements expected.
## Acceptance
- [ ] Invariants hold; no leaks.