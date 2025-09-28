---
title: A11/k1 — observer_ptr basics
kit_id: a11_implicit_mgmt_variants
version: 1.0
status: Draft
type: kata
---
## Goal
Wrap raw pointer in observer_ptr and test comparisons/null handling.
## Task
Use observer_ptr<int> p; assign, compare, reset.
## Acceptance
- [ ] observer_ptr behaves like raw; nullptr valid; no delete.