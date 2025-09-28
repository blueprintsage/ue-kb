---
title: B6/k20 — noexcept swap policy & vector growth paths
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Demonstrate how `noexcept(move)` controls `std::vector` reallocation strategies.
## Acceptance
- [ ] With noexcept(true) moves, vector grows using move; with noexcept(false) it falls back to copy; tests detect the behavior via counters.
