---
title: C3/k5 — scalable_allocator
kit_id: c3_containers_allocators
version: 1.0
status: Draft
type: kata
---
## Goal
Measure time/alloc counts for small objects.
## Task
Use STL `vector<string>` with default vs `tbb::scalable_allocator`.
## Acceptance
- [ ] Scalable allocator reduces upstream allocations or time.