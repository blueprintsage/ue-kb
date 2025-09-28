---
title: B11/k4 — ADL hijack & safe calling pattern
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Demonstrate unwanted ADL resolution; fix with qualified calls, `std::swap` via using+ADL, or detail namespace shims.
## Acceptance
- [ ] Bad variant calls wrong overload; safe wrapper calls intended function across TU boundaries.
