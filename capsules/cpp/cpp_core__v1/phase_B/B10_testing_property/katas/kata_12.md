---
title: B10/k12 — noexcept move & strong exception safety
kit_id: b10_resources
version: 1.0
status: Draft
type: kata
---
## Objective
Mark moves `noexcept` where valid to enable container fast paths.
## Acceptance
- [ ] Vector reallocation uses move not copy when `noexcept(true)`; tests detect via counters; invariants preserved on throw.
