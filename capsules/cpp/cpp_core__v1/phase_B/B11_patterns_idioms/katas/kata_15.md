---
title: B11/k15 — Macros that change meaning (side effects)
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Demonstrate macro side-effects/double-eval; replace with `constexpr`/inline functions.
## Acceptance
- [ ] Bad macro fails with duplicated side effects; refactor passes and is safer under debugging/tools.
