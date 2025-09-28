---
title: B1/k6 — Smart Pointers 101 (unique/shared/weak)
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Pick the right smart ptr for ownership patterns.
## Tasks
- Replace raw owning pointer with `std::unique_ptr`; add shared view with `std::weak_ptr` to break cycles.
## Acceptance
- [ ] Ownership diagram matches code; tests show no leaks/cycles.