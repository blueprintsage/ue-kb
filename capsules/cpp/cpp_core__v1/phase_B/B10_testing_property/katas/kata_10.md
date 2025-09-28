---
title: B10/k10 — span & contiguous range interop
kit_id: b10_resources
version: 1.0
status: Draft
type: kata
---
## Objective
Expose non-owning views with `std::span` safely.
## Acceptance
- [ ] No dangling spans; tests ensure source outlives span; zero-copy handoff to C APIs via `data()/size()`.
