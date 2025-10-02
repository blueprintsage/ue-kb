---
title: A8/k5 — alignment guarantees
kit_id: a8_allocators_arenas
version: 1.0
status: Draft
type: kata
---
## Goal
Prove `alignof(T)` respected for several T (char, double, max_align_t).
## Task
Allocate for each T; assert `(uintptr_t(ptr) % alignof(T) == 0)`.
## Acceptance
- [ ] All align checks pass under sanitizer.