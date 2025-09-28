---
title: A12/k8 — perf sanity check
kit_id: a12_pmr_custom_resources
version: 1.0
status: Draft
type: kata
---
## Goal
Time hot path with/without PMR and ensure no correctness regressions.
## Task
Pick container workload; compare timings; assert same results.
## Acceptance
- [ ] PMR path is equal or faster without behavior change.