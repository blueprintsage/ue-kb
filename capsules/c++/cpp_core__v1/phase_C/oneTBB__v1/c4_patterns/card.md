---
title: C4 — Patterns (Pipelines, for_each, Reductions)
kit_id: c4_patterns
version: 1.0
status: Draft
category: Concurrency
assets: []
dependencies: [c1_tasks_arenas, c2_flow_graph]
---


## Objective
Apply reusable concurrency patterns with oneTBB: build pipelines (with Flow Graph), `parallel_for_each`, `parallel_reduce`, map/reduce, and fan‑in/fan‑out templates; add determinism guards.


## Setup
- oneTBB (>= 2021); Catch2 for tests.


## Steps
1) **Pipeline pattern**: source → transform → filter → sink via Flow Graph; back‑pressure with limiter.
2) **parallel_for_each**: partition work over ranges; set grainsize; compare serial vs parallel.
3) **parallel_reduce**: associative/commutative combine; deterministic results.
4) **Map→Reduce**: two‑phase job using containers + algorithms; minimize contention.
5) **Fan‑in barrier**: merge results with a `continue_node` barrier.
6) **Determinism guard**: design tests to ensure order‑independent correctness.


## Smoke Test
- [ ] Pipeline produces same outputs as serial baseline.
- [ ] Reductions equal reference across runs.


## Blueprint Hook (TL;DR for BP users)
**What transfers:** break problems into map/transform/reduce; guard for determinism; test serial baseline vs parallel.
**BP building blocks:** ForEach loops, Async Tasks, and a final “merge” step on game thread.


## Keep/Revert
KEEP: determinism template; REVERT: skip pipeline if Flow Graph not available.