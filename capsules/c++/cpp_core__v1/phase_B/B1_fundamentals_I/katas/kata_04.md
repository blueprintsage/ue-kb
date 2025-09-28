---
title: B1/k3 — Const‑Correctness (APIs & Internals)
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Design API with `const` where promised; use `mutable` only for caches.
## Tasks
- Provide const/non‑const accessors; ensure thread‑safe cache with `mutable` + atomics or guards.
## Acceptance
- [ ] `const` objects call only `const` methods; caches don’t break visible state.