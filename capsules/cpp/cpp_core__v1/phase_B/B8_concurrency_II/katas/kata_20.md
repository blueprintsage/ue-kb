---
title: B8/k20 — Allocator-aware container (arena/region)
kit_id: b8_perf_layout
version: 1.0
status: Draft
type: kata
---
## Objective
Build a simple arena allocator and use it in a container.
## Acceptance
- [ ] Arena-backed container reduces alloc/free calls; teardown releases in O(1).
