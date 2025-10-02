---
title: B10 — Resource Patterns (RAII & Ownership)
kit_id: b10_resources
version: 1.0
status: Draft
category: C++ Core
assets: []
dependencies: []
---

## Objective
Model ownership crisply with RAII: design leak-free, exception-safe types; document aliasing; and make lifetimes obvious at call sites.

## Steps
1) RAII handles: unique/shared/weak; custom deleters; intrusive refcounting.
2) Encapsulation: pImpl, handle/body, type erasure with small-buffer.
3) Allocation: allocator-aware types; `std::pmr` basics; arenas/regions.
4) Interop: spans and contiguous ranges; C APIs (`data()`/`size()`), file/mmap.
5) API design: move/copy/noexcept; ref-qualified & value-category aware interfaces.

## Smoke Test
- [ ] All katas pass sanitizers; no leaks under ASan/LSan.  
- [ ] Moves are `noexcept` where valid; aliasing rules and lifetimes documented.

## Notes
Prefer **single, obvious ownership**. Keep destructors lightweight and `noexcept(true)`. Never expose raw owning pointers across API boundaries.
