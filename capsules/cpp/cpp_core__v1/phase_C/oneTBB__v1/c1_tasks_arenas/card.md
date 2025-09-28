---
title: C1 — oneTBB: Tasks & Arenas
kit_id: c1_tasks_arenas
version: 1.0
status: Draft
category: Concurrency
assets: []
dependencies: []
---


## Objective
Use **oneTBB** to run work with task groups and arenas: `task_group`, `parallel_for`, `task_arena`, thread limits, priorities, cancellation, `isolate`, and nested parallelism rules.


## Setup
- oneTBB (tbb >= 2021). Link against TBB; enable `-O2 -g -pthread`.
- Test: Catch2; use a shared counter guarded by atomics for correctness checks.


## Steps
1) **Warm‑up**: run a simple `parallel_for` over N elements; verify sum.
2) **task_group**: spawn two independent tasks; wait; confirm deterministic result.
3) **task_arena**: create arenas with different concurrency (e.g., 1, 2, default); observe throughput & fairness.
4) **Priorities**: submit high vs normal; measure ordering impact (best‑effort, not strict).
5) **Cancellation**: cancel a long loop from another task; ensure tasks check tokens and exit promptly.
6) **isolate**: protect a critical region of tasks from stealing; compare before/after timings.
7) **Nested parallelism**: show that nested `parallel_for` inside an arena doesn’t deadlock; use `task_arena::execute`.


## Smoke Test
- [ ] Results correct across runs (atomic checks).
- [ ] Cancellation shortens wall time vs uncancelled.
- [ ] Arena(1) behaves like a single‑thread executor.


## Blueprint Hook (TL;DR for BP users)
**What transfers:** break work into small jobs; run on a pool; avoid doing heavy work on the game thread.
**BP building blocks:** Async Tasks (Blueprint latent actions), timers, task queues via C++ subsystem exposed to BP.
**Mini demo:** Queue 1,000 lightweight jobs; tick a progress bar on the game thread; Acceptance: UI stays responsive and completes with correct count.


## Keep/Revert
KEEP: explicit arena sizing + cancellation token pattern.
REVERT: drop priorities if your TBB build lacks it.