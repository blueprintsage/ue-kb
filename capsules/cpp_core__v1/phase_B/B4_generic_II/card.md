---
title: B4 — Generic II (ranges, views, iterators)
kit_id: b4_generic_II
version: 1.0
status: Draft
category: C++ Core
assets: []
dependencies: []
---


## Objective
Use **C++20 Ranges** to write clear, lazy pipelines; understand iterator categories; build custom views and adaptors safely.


## Steps
1) **Range basics:** `ranges::begin/end`, `range` concept, borrowing.
2) **Pipelines:** `views::filter/transform/take/drop/chunk/slide/zip`.
3) **Ownership & lifetimes:** borrowed vs owning views; dangling.
4) **Custom views:** view facade/adaptor closure; iterator & sentinel.
5) **Algorithms:** `ranges::` versions; projections; `ranges::to` (helper).
6) **Iterators:** categories, iterator_traits; contiguous vs random‑access.


## Smoke Test
- [ ] Pipelines compile on Clang/GCC/MSVC; no dangling iterators.
- [ ] Custom view passes range concepts and works in algorithms.


## Notes
Prefer composing **views** for lazy work; materialize intentionally with `ranges::to<container>()` or `std::vector(v | views::...)`.