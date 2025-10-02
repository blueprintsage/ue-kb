---
title: A12/k2 — unsynchronized_pool_resource
kit_id: a12_pmr_custom_resources
version: 1.0
status: Draft
type: kata
---
## Goal
Use pool resource for many small objects.
## Task
Allocate many tiny strings/nodes; compare time/allocs vs default.
## Acceptance
- [ ] Pool shows fewer upstream allocations and better time for small objects.