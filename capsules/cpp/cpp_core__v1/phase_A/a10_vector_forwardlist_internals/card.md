---
title: A10 — Vector & ForwardList Internals
kit_id: a10_vector_forwardlist
version: 1.0
status: Draft
category: Containers & Performance
assets: []
dependencies: [a2_unique_ptr_deleters, a8_allocators_arenas]
---


## Objective
Understand `std::vector` growth strategies, capacity vs size, iterator/iterator invalidation rules, relocation/move semantics for element types, and `std::forward_list` tradeoffs (single-linked list, splice, constant-time insert after). Learn micro-optimizations and how to choose between contiguous vs linked containers.


## Setup
- Tooling: Catch2, optional microbench with `std::chrono` timing.
- Compile with `-O2`; run under sanitizers for safety when testing relocations.


## Steps
1) **Growth policies:** experiment with geometric growth factors; implement a toy `vector` growth policy to observe realloc counts and total allocations.
2) **Relocation vs Move/Copy:** test types that are `noexcept` movable vs throwing move/only-copy; verify when `std::vector` uses `memmove` vs element move/construct/destroy.
3) **Reserve & shrink_to_fit:** measure capacity changes and how `shrink_to_fit` behaves (non-binding request).
4) **Iterator invalidation:** map operations to invalidation rules; test loops that keep references/pointers across push_back and document safe patterns.
5) **Forward_list ops:** demonstrate `splice_after`, `insert_after`, `erase_after`, and use-cases where forward_list outperforms vector (no realloc, cheap insert after known iterator).
6) **Cache/locality tradeoff:** microbench insertion/iteration across sizes to see vector vs forward_list traversal speed.
7) **Acceptance tests:** set of deterministic tests that assert semantics (relocation counts, iterator invalidation behavior, splice correctness).


## Smoke Test
- [ ] Toy growth policy reproduces allocation counts for N pushes.
- [ ] Relocation path confirmed (memmove vs move ctors) for trivially relocatable types.
- [ ] Forward_list splice preserves element order and no leaks.


## Blueprint Hook (TL;DR for BP users)
**What transfers:** contiguous storage (vector) = arrays/fast random access; linked lists = cheap local inserts when you hold an iterator.
**BP building blocks:** arrays, TArray in Unreal (reserve(), Emplace), spawning actor pools vs linked event chains.
**Mini demo:** Use an array/ TArray reserve to pre-allocate enemy slots; Acceptance: no per-spawn allocation during wave.


## Keep/Revert
KEEP: relocation/memmove demonstration.
REVERT: drop microbench if CI time constrained.