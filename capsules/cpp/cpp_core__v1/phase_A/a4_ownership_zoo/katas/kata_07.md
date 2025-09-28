---
title: A4/k7 — guard dangling observers
kit_id: a4_ownership_zoo
version: 1.0
status: Draft
type: kata
---
## Goal
Detect and avoid using observers after owner destruction.
## Task
Hold `Widget* obs` to an owned Widget; destroy owner; show UB risk; then fix by nulling observer via callback or using `weak_ptr` in the shared case.
## Acceptance
- [ ] Fixed version avoids deref after destroy (no ASan hit).