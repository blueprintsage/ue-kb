---
title: B11/k24 — UB from uninitialized memory & memcpy of non-trivial
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Show UB from using uninitialized data and from `memcpy` of non-trivially copyable types; fix with constructors/`std::bit_cast` rules.
## Acceptance
- [ ] UBSan/Valgrind flags pre-fix; corrected construction/copy passes; note triviality requirements in comments.
