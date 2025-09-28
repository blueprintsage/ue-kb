---
title: B8/k15 — Lookup structures: flat_map vs std::map
kit_id: b8_perf_layout
version: 1.0
status: Draft
type: kata
---
## Objective
Compare cache-friendly flat structures vs node-based maps.
## Acceptance
- [ ] flat_map wins for read-heavy small N; tradeoffs documented for large N/writes.
