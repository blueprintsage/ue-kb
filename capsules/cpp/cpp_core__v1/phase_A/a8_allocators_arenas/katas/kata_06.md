---
title: A8/k6 — stats & scope guard
kit_id: a8_allocators_arenas
version: 1.0
status: Draft
type: kata
---
## Goal
Track bytes/allocs and report deltas for a block of work.
## Task
Add counters to arena; create `arena_scope` RAII capturing start/stop; test peak and delta.
## Acceptance
- [ ] Reported stats match expectations in tests.