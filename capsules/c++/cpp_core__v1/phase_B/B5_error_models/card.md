---
title: B5 — Iterators & Ranges (modern algorithms)
kit_id: b5_ranges
version: 1.0
status: Draft
category: C++ Core
assets: []
dependencies: []
---

## Objective
Use C++20 **Ranges** and iterator concepts to write safe, composable algorithms and custom views, avoiding lifetime traps.

## Steps
1) Iterator concepts & categories; traits; contiguous vs random-access.
2) Core views: transform, filter, take/drop, chunk/slide, zip/join.
3) Borrowed vs owning ranges; dangling and how to prevent it.
4) Build a minimal custom iterator and a sentinel; then a small view.
5) Compose pipelines with projections and `ranges::` algorithms.

## Smoke Test
- [ ] Pipelines compile (Clang/GCC/MSVC) and produce expected sequences.  
- [ ] Custom iterator/view satisfy required concepts and pass algorithms.

## Notes
Favor lazy **views**; only materialize intentionally. Be explicit about lifetimes—prefer borrowed or owning types instead of piping temporaries that will dangle.
