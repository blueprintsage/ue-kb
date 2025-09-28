---
title: B9/k16 — Parallel for (chunking & affinity)
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Split range into chunks; avoid false sharing; maintain affinity where helpful.
## Acceptance
- [ ] Speedup vs single-thread on N>1; results correct; chunksize tuning logged.
