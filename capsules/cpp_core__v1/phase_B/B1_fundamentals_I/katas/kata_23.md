---
title: B1/k23 — `std::array` vs `std::vector`
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Pick fixed vs dynamic sequence containers appropriately.
## Tasks
- Replace small fixed buffer with `std::array`; profile stack vs heap.
## Acceptance
- [ ] Correct semantics; stack use reduces allocations where intended.