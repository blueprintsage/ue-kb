---
title: B4/k28 — Contiguous Range Interop (C APIs)
kit_id: b4_generic_II
version: 1.0
status: Draft
type: kata
---
## Objective
Expose `data()`/`size()` pairs safely to C APIs; avoid lifetime bugs.
## Acceptance
- [ ] No dangling pointers; static analysis clean.