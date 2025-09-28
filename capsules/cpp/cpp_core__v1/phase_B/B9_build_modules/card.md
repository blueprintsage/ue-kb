---
title: B9 — Concurrency Essentials (correctness first)
kit_id: b9_concurrency
version: 1.0
status: Draft
category: C++ Core
assets: []
dependencies: []
---

## Objective
Use standard C++ concurrency tools safely—threads, atomics, and synchronization—prioritizing correctness (no data races, deadlocks, or ABA) and debuggability.

## Steps
1) Threads & cancellation: `std::thread`/`std::jthread`, `stop_token`, join/RAII.
2) Synchronization: mutexes, `scoped_lock`, condition variables, barriers/latches.
3) Atomics: memory orders (relaxed/acquire-release/seq_cst), fences, hazards.
4) Async: futures/promises, packaged_task; task pipelines.
5) Contention & false sharing: alignment, work partitioning; testing with TSan.

## Smoke Test
- [ ] All katas pass ThreadSanitizer where applicable; deadlock tests reproduce then fix; deterministic seeds used for flaky races.

## Notes
Keep critical sections tiny; never call user code while holding a lock; prefer structured cancellation via `stop_token`.
