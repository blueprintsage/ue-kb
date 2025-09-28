---
title: B1/k16 — Strong Typedefs (`struct` wrappers)
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Wrap primitive IDs/units to prevent mixups.
## Tasks
- Create `struct Meters{double;}` vs `struct Seconds{double;}`; overload ops intentionally.
## Acceptance
- [ ] Cross‑use fails to compile; correct ops succeed.