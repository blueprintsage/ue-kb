---
title: B1/k12 — Lifetime Extension & References to Temporaries
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Use `const T&` to extend temporary lifetimes safely; avoid dangling.
## Tasks
- Contrast binding to `const&` vs storing pointer/ref; add tests that fail on UB via sanitizers.
## Acceptance
- [ ] No dangling; sanitizer stays silent.