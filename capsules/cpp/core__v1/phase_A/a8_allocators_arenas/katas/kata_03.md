---
title: A8/k3 — STL adapter allocator
kit_id: a8_allocators_arenas
version: 1.0
status: Draft
type: kata
---
## Goal
Use `arena_allocator<T>` with `std::vector<T>`.
## Task
Implement `value_type`, `allocate`, `deallocate`, `rebind`; construct vector with it and run push_backs.
## Acceptance
- [ ] Vector ops succeed; arena stats show usage.