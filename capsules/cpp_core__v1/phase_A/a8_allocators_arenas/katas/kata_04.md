---
title: A8/k4 — overflow: throw vs fallback
kit_id: a8_allocators_arenas
version: 1.0
status: Draft
type: kata
---
## Goal
Decide behavior when arena is full.
## Task
Build two modes: (A) throw bad_alloc; (B) delegate to global new. Verify via tests.
## Acceptance
- [ ] Both modes behave as configured; no silent corruption.