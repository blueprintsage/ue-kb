---
title: A8/k1 — bump arena
kit_id: a8_allocators_arenas
version: 1.0
status: Draft
type: kata
---
## Goal
Implement a contiguous bump arena with `allocate(n, align)` and `reset()`.
## Task
Back with `std::vector<std::byte>`; maintain head pointer; honor alignment.
## Acceptance
- [ ] Allocations return distinct, aligned regions; reset frees all at once.