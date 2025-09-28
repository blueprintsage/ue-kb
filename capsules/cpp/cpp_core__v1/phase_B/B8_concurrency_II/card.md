---
title: B8 — Performance & Data Layout (practical speed)
kit_id: b8_perf_layout
version: 1.0
status: Draft
category: C++ Core
assets: []
dependencies: []
---

## Objective
Make code measurably faster by fixing data layout, allocation, and branch behavior—using disciplined microbenchmarks (p50/p95) and clear before/after evidence.

## Steps
1) Baseline: copy vs move, small-object behavior, branchy vs table-driven.
2) Data layout: AoS↔SoA, packing/alignment, cache-friendly traversal.
3) Allocation: pools/arenas/pmr; vector growth; small-buffer optimizations.
4) Hot paths: inlining, constexpr precompute, SIMD intro, prefetch hints.
5) Measurement: harness, stable seeds/data, p50/p95, regression guards.

## Smoke Test
- [ ] Each kata logs baseline and tuned metrics; speedups justified by counters/tables.  
- [ ] CI perf guard prevents >10% regressions where specified.

## Notes
Never benchmark in Debug. Keep datasets deterministic. Optimize data first; algorithms second; micro-ops last.
