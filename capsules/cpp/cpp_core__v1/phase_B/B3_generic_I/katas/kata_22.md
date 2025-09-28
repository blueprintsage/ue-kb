---
title: B3/k21 — Heterogeneous Lookup (Transparent)
kit_id: b3_generic_I
version: 1.0
status: Draft
type: kata
---
## Objective
Create a transparent comparator for maps/sets to avoid allocations.
## Acceptance
- [ ] Lookups by `std::string_view` avoid constructing `std::string`.