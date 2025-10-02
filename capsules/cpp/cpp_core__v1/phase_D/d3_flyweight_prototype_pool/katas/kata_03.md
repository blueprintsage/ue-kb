---
title: D3/k3 — Object pool
kit_id: d3_flyweight_prototype_pool
version: 1.0
status: Draft
type: kata
---
## Goal
Pre‑allocate and reuse objects safely.
## Task
Implement pool with free list and poison; test exhaustion and reuse.
## Acceptance
- [ ] No double‑free; exhaustion handled.