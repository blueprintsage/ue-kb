---
title: B5/k3 — bounded_view (begin, end, size)
kit_id: b5_ranges
version: 1.0
status: Draft
type: kata
---
## Objective
Create a simple `bounded_view` that restricts iteration to [lo, hi).
## Acceptance
- [ ] Iteration stops at bound; `size()` equals hi - lo; works in `ranges::for_each`.
