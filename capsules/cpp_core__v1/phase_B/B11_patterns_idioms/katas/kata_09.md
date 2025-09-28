---
title: B11/k9 — UB casts (reinterpret_cast & strict aliasing)
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Demonstrate aliasing UB and fix using byte view, `std::bit_cast`, or variant/union-as-bytes.
## Acceptance
- [ ] UB path triggers sanitizer; safe cast pattern passes with identical observable behavior.
