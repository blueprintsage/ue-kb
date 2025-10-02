---
title: A0/k1 — string_view dangling guard
kit_id: a0_on_ramp
version: 1.0
status: Draft
type: kata
---
## Goal
Detect and prevent a dangling `std::string_view`.
## Task
Write a helper that only returns `string_view` tied to a persistent `string`.
## Acceptance
- [ ] A failing test demonstrates a dangling view (ASan hit).
- [ ] A passing test uses a persistent buffer and succeeds.