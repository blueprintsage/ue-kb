---
title: C3/k6 — cache_aligned_allocator
kit_id: c3_containers_allocators
version: 1.0
status: Draft
type: kata
---
## Goal
Reduce false sharing on arrays of structs.
## Task
Allocate with `tbb::cache_aligned_allocator<T>`; measure contention.
## Acceptance
- [ ] Lower contention / better throughput vs default.