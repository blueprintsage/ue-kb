---
title: A8 — Allocators & Arenas
kit_id: a8_allocators_arenas
version: 1.0
status: Draft
category: Resource Management
assets: []
dependencies: [a1_raii, a2_unique_ptr_deleters, a4_ownership_zoo, a5_new_delete_variants]
---

## Objective
Design and plug custom allocators/arenas into standard containers to reduce fragmentation, improve locality, and bound allocation costs. Cover **bump/arena**, **pool/freelist**, adapter allocators for STL, and light‑weight stats.

## Setup
- Tooling: Catch2; optional microbench.
- Build flags: `-O2 -g` when timing; sanitize for correctness otherwise.

## Steps
1) **Bump arena**: single contiguous buffer; `allocate(n)` bumps pointer; `deallocate` no‑op; `reset()` clears all.
2) **Pool allocator**: fixed‑size blocks from free list; O(1) alloc/free; good for many same‑sized objects.
3) **STL adapter**: make `template<class T> struct arena_allocator` forwarding to the bump arena; use with `std::vector<T, arena_allocator<T>>`.
4) **Fallback/overflow**: when arena is full, either throw or fallback to `::operator new` (configurable); test both.
5) **Alignment**: round allocations to `alignof(T)`; prove no UB via `std::align`.
6) **Stats & guardrails**: track peak bytes, alloc count; assert on double‑free in pool; provide RAII scope to snapshot deltas.

## Smoke Test
- [ ] Containers work with custom allocator; all tests pass under ASan/UBSan.  
- [ ] Alignment correct; no dangling pointers from arena reset outside its lifetime.

## Blueprint Hook (TL;DR for BP users)
**What transfers:** group allocations into **sessions** and release them in one go to avoid leaks/fragmentation.  
**BP building blocks:** Level streaming chunks; pooled actors/components; `NiagaraSystem` instance pooling.  
**Mini demo:** Spawn 200 pooled actors for a wave (session), then free all by destroying pool owner; Acceptance: perf spike happens once at start, not per spawn.

## Keep/Revert
KEEP: Overflow strategy switch.  
REVERT: Microbench if CI time is tight.