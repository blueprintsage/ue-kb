---
title: B1/k21 — `std::optional` for Nullable Value Semantics
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Prefer `optional<T>` over raw pointers for “maybe” values.
## Tasks
- Replace pointer‑nullable param with `optional<T>`; benchmark branch/size cost.
## Acceptance
- [ ] Clearer API; no null deref paths; perf acceptable.