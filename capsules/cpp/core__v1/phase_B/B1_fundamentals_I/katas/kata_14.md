---
title: B1/k14 — `=default` vs hand‑written (ABI & Semantics)
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Prefer `= default` where behavior equals compiler‑generated.
## Tasks
- Replace manual trivial ctor/dtor with `= default`; verify identical behavior and smaller codegen.
## Acceptance
- [ ] Tests unchanged; binary size same or smaller.