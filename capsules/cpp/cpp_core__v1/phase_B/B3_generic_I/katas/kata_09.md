---
title: B3/k9 — Non‑type Template Parameters (NTTP)
kit_id: b3_generic_I
version: 1.0
status: Draft
type: kata
---
## Objective
Use NTTP for fixed‑size arrays and policy toggles.
## Acceptance
- [ ] `buffer<int,64>` allocates on stack; `static_assert(sizeof==64*sizeof(int))`.