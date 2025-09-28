---
title: B8/k14 — Data-locality friendly iteration order
kit_id: b8_perf_layout
version: 1.0
status: Draft
type: kata
---
## Objective
Pick loop order matching memory layout (row-major/column-major).
## Acceptance
- [ ] Correctness equal; locality order wins for large matrices; p95 logged.
