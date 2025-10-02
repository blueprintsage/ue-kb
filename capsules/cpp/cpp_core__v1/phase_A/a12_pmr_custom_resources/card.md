---
title: A12 — PMR & Custom Resources
kit_id: a12_pmr_custom_resources
version: 1.0
status: Draft
category: Resource Management
assets: []
dependencies: [a8_allocators_arenas]
---


## Objective
Use **`std::pmr`** to route allocations through polymorphic memory resources: monotonic buffers, unsynchronized pools, and custom `memory_resource` that tracks stats or forwards to arenas. Learn how to swap resources at runtime and confine allocation to a scope.


## Setup
- Tooling: Catch2; enable `-O2` for light timing tests.


## Steps
1) **Monotonic buffer resource**: back with `std::pmr::monotonic_buffer_resource` and tie to containers via `pmr::vector`.
2) **Unsynchronized pool resource**: use `pmr::unsynchronized_pool_resource` for many small allocations; measure perf vs default.
3) **Custom resource**: derive from `pmr::memory_resource` to add simple stats (bytes, alloc count), forward to upstream.
4) **Scoped resource switch**: create an RAII guard that sets a thread-local default resource and restores it on exit.
5) **Arena bridge**: adapt your A8 bump arena behind a `memory_resource` façade.


## Smoke Test
- [ ] pmr::vector uses the given resource; stats reflect allocations.
- [ ] Monotonic resets free all; pool resource reuses blocks.


## Blueprint Hook (TL;DR for BP users)
**What transfers:** pick a buffer/pool per **scene/session** and route all work through it; clear in one step.
**BP building blocks:** subsystem/manager owns arrays of pooled actors/components; reset on level change.
**Mini demo:** One shared “FX session” pool; all temporary arrays pull from it; clear at end; Acceptance: stable frame times, no spikes mid-session.


## Keep/Revert
KEEP: Custom resource with stats + arena bridge.
REVERT: If pmr not available on target toolchain, provide a shim or skip.