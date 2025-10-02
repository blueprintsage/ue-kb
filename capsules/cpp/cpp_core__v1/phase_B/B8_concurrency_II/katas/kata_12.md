---
title: B8/k12 — Object layout: packing & alignment
kit_id: b8_perf_layout
version: 1.0
status: Draft
type: kata
---
## Objective
Reorder fields to minimize padding; align hot data.
## Acceptance
- [ ] Size reduction demonstrated; alignment avoids false sharing in array-of-objs test.
