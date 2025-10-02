---
title: C3/k1 — concurrent_unordered_map
kit_id: c3_containers_allocators
version: 1.0
status: Draft
type: kata
---
## Goal
Insert N keys in parallel and validate lookups.
## Task
Use `parallel_for` to insert; then parallel find and count.
## Acceptance
- [ ] All keys present; no races.