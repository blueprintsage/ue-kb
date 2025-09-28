---
title: B1/k18 — Overload Sets & `using std::swap`
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Get ADL‑friendly swap; avoid hijacking std.
## Tasks
- Implement custom `swap(T&,T&)`; bring `using std::swap;` then `swap(a,b)`; confirm ADL picks ours.
## Acceptance
- [ ] Correct swap chosen; no UB by specializing in `std`.