---
title: C2 — Flow Graph
kit_id: c2_flow_graph
version: 1.0
status: Draft
category: Concurrency
assets: []
dependencies: [c1_tasks_arenas]
---


## Objective
Model data‑flow with **oneTBB Flow Graph**: `function_node`, `broadcast_node`, `buffer_node`, `queue_node`, `join_node`, `sequencer_node`, `limiter_node`, edges and back‑pressure, cancellation, and exception safety.


## Setup
- oneTBB (>= 2021). Build with `-O2 -g -pthread`.
- Tests: Catch2; use atomic counters for correctness.


## Steps
1) **Linear pipeline**: source → transform → sink via `function_node` chain; verify end‑to‑end counts.
2) **Fan‑out**: use `broadcast_node` to feed two consumers; combine results in a sink.
3) **Buffering**: insert `buffer_node` or `queue_node` between stages to decouple producers/consumers.
4) **Ordering**: use `sequencer_node` to enforce processing order; compare with unordered execution.
5) **Join**: zip two streams with `join_node` (tagged/queue‑based); prove alignment of pairs.
6) **Limiter/back‑pressure**: gate inflow with `limiter_node`; increment tokens after sink finishes.
7) **Concurrency**: set node concurrency (serial vs unlimited); measure throughput vs determinism.
8) **Cancellation**: call `g.cancel();` and ensure nodes exit and `g.wait_for_all()` returns; clean up state.
9) **Exceptions**: throw in a node; confirm graph unwinds and reports; guard shared state.


## Smoke Test
- [ ] Fan‑out produces correct combined result.
- [ ] Join pairs align by key.
- [ ] Cancellation/exception tests leave graph in a joinable state.


## Blueprint Hook (TL;DR for BP users)
**What transfers:** treat gameplay events as a graph: sources → processors → sinks; throttle inputs when sinks are busy.
**BP building blocks:** Event dispatchers, Timers, Async tasks; `Gate`/`Branch` nodes for back‑pressure.
**Mini demo:** Fire events into two processors (log + analytics) and join at a counter; Acceptance: counts match, no UI hitching.


## Keep/Revert
KEEP: limiter + join patterns. REVERT: drop `sequencer_node` if API version lacks it.