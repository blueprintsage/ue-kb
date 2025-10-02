---
title: D3/k5 — Bulk teardown
kit_id: d3_flyweight_prototype_pool
version: 1.0
status: Draft
type: kata
---
## Goal
Release entire pool at once.
## Task
Provide `reset()` to free all; verify no leaks and reusable after reset.
## Acceptance
- [ ] Reset leaves pool empty; next usage ok.