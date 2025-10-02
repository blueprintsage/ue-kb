---
title: B11/k14 — Copy elision assumptions & NRVO pitfalls
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Show reliance on elision can break with different compilers/flags; design for correctness without it.
## Acceptance
- [ ] Counters prove extra moves/copies in bad path; corrected version passes with stable semantics.
