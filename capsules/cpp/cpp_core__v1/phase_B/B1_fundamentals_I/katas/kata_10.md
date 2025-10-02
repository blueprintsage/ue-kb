---
title: B1/k10 — Copy Elision & NRVO
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Observe guaranteed copy elision and Named Return Value Optimization.
## Tasks
- Return heavy object by value; instrument ctor/move; compare builds with/without optimizations.
## Acceptance
- [ ] Zero copies when elision applies; moves only where required.