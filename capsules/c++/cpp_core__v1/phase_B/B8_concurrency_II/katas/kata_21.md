---
title: B8/k21 — IO buffering & batching
kit_id: b8_perf_layout
version: 1.0
status: Draft
type: kata
---
## Objective
Batch writes/reads to cut syscalls.
## Acceptance
- [ ] Buffered IO beats unbuffered by ≥2× on synthetic workload; flush policy documented.
