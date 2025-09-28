---
title: B11/k1 — Narrowing conversions & silent truncation
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Reproduce narrowing (e.g., double→int, uint32_t→uint8_t) and fix with explicit, checked casts.
## Acceptance
- [ ] With `-Wconversion`, bad path warns/fails; safe cast path passes and preserves bounds.
