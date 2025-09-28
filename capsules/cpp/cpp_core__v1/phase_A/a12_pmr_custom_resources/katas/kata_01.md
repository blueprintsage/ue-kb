---
title: A12/k1 — monotonic + pmr::vector
kit_id: a12_pmr_custom_resources
version: 1.0
status: Draft
type: kata
---
## Goal
Back a pmr::vector with a monotonic buffer.
## Task
Construct `monotonic_buffer_resource buf; pmr::vector<int> v{&buf};` push N; reset buffer.
## Acceptance
- [ ] Reset frees all vector storage at once.