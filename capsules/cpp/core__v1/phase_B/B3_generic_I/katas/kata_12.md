---
title: B3/k12 — Detection Idiom (void_t)
kit_id: b3_generic_I
version: 1.0
status: Draft
type: kata
---
## Objective
Detect presence of `begin/end` members SFINAE‑style.
## Acceptance
- [ ] `has_begin_v<T>` works for containers and fails for int.