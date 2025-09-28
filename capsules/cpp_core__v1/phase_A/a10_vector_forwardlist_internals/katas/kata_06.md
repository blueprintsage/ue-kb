---
title: A10/k6 — stable references via index indirection
kit_id: a10_vector_forwardlist
version: 1.0
status: Draft
type: kata
---
## Goal
Show pattern: store stable handles (indices or indirection) instead of raw pointers to avoid invalidation.
## Task
Keep `vector<T>` with parallel `vector<int> handle_to_pos`; simulate removals by swapping-with-last and update handles.
## Acceptance
- [ ] No dangling refs; lookups via handle return correct element.