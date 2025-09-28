---
title: C3 — Containers & Allocators
kit_id: c3_containers_allocators
version: 1.0
status: Draft
category: Concurrency
assets: []
dependencies: []
---


## Objective
Use oneTBB concurrent containers (`concurrent_unordered_map/set`, `concurrent_vector`, `concurrent_queue`, `concurrent_priority_queue`) and allocators (`scalable_allocator`, `cache_aligned_allocator`) for safe parallel access and better locality.


## Setup
- oneTBB (>= 2021). Build with `-O2 -g -pthread`.
- Tests: Catch2; atomics for validation.


## Steps
1) **concurrent_unordered_map**: parallel insert/find; accessor API for safe updates.
2) **concurrent_vector**: `grow_by`, `push_back` in parallel; reserve and iterate.
3) **concurrent_queue**: MPMC producer/consumer; non‑blocking semantics.
4) **concurrent_priority_queue**: custom comparator; push/pop under contention.
5) **Allocators**: plug `scalable_allocator`/`cache_aligned_allocator` into STL containers and measure throughput.
6) **Iteration & snapshots**: safe iteration patterns without stopping producers.


## Smoke Test
- [ ] No data races under ThreadSanitizer or invariants.
- [ ] Throughput improves with TBB allocators on many small objects.


## Blueprint Hook (TL;DR for BP users)
**What transfers:** choose data structures that handle contention; decouple producer/consumer.
**BP building blocks:** queues for gameplay events, arrays for actor pools; avoid shared writes on the game thread.


## Keep/Revert
KEEP: allocator plug‑ins; REVERT: skip priority queue if not available on platform.