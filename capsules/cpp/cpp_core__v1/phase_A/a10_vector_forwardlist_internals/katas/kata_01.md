---
title: A10/k1 — growth policy counts
kit_id: a10_vector_forwardlist
version: 1.0
status: Draft
type: kata
---
## Goal
Implement toy vector that counts reallocations for different growth factors (1.5x, 2x, 1.25x).
## Task
Push N elements; report alloc count and total allocated bytes per policy.
## Acceptance
- [ ] Reports show expected fewer reallocations for larger factors but higher peak memory.