---
title: B10/k6 — pmr::polymorphic_allocator basics
kit_id: b10_resources
version: 1.0
status: Draft
type: kata
---
## Objective
Use `pmr::monotonic_buffer_resource` and compare to default allocator.
## Acceptance
- [ ] Allocation count drops; resource lifetime clear; no use-after-free with short-lived pools.
