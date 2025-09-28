---
title: B10/k11 — Ref-qualified member APIs (& and &&)
kit_id: b10_resources
version: 1.0
status: Draft
type: kata
---
## Objective
Design APIs that differ for lvalues/rvalues to prevent accidental copies.
## Acceptance
- [ ] `foo().get()` returns by value; `x.get()` returns by ref; misuse caught at compile time via overload set.
