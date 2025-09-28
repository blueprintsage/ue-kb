---
title: B11/k5 — Implicit conversions & bool traps
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Prevent accidental conversion to bool or between unrelated types using `explicit` and strong types.
## Acceptance
- [ ] Bad path compiles but fails test; adding `explicit`/strong typedef fixes and tests pass.
