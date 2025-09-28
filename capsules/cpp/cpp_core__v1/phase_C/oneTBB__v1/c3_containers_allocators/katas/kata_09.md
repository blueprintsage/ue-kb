---
title: C3/k9 — map + parallel reduce
kit_id: c3_containers_allocators
version: 1.0
status: Draft
type: kata
---
## Goal
Combine containers with TBB algorithms.
## Task
Fill map concurrently; compute aggregate with `parallel_for` + atomics.
## Acceptance
- [ ] Aggregate equals sequential reference.