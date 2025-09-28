---
title: A8/k2 — pool allocator
kit_id: a8_allocators_arenas
version: 1.0
status: Draft
type: kata
---
## Goal
Fixed‑block pool with push/pop free list.
## Task
Pre‑allocate N blocks; `allocate()` pops; `deallocate(p)` pushes with poison/checks.
## Acceptance
- [ ] O(1) alloc/free; double‑free detected in tests.