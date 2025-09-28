---
title: B8/k3 — AoS → SoA transform
kit_id: b8_perf_layout
version: 1.0
status: Draft
type: kata
---
## Objective
Convert array-of-structs to struct-of-arrays and compare traversal speed.
## Acceptance
- [ ] SoA traversal beats AoS p95 on synthetic data; correctness retained.
