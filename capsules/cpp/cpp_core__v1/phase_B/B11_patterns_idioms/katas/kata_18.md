---
title: B11/k18 — constexpr pitfalls (UB/ODR in constant eval)
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Trigger invalid constant evaluation (e.g., ODR-use of non-literal); fix with literal types and pure functions.
## Acceptance
- [ ] Compile error reproduced; corrected constexpr design compiles across major compilers.
