---
title: B4/k3 — Projections in ranges::sort
kit_id: b4_generic_II
version: 1.0
status: Draft
type: kata
---
## Objective
Use projections to sort by field without custom comparator.
## Acceptance
- [ ] `ranges::sort(vec, {}, &T::field)` sorts correctly.