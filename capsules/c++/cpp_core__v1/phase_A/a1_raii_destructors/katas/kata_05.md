---
title: A1/k5 — destructor order (inheritance)
kit_id: a1_raii
version: 1.0
status: Draft
type: kata
---
## Goal
Observe base/derived destruction and virtual destructor needs.
## Task
Log order; add `virtual ~Base()` and compare.
## Acceptance
- [ ] Expected order confirmed by asserts/logs.