---
title: A5/k4 — aligned new/delete
kit_id: a5_new_delete_variants
version: 1.0
status: Draft
type: kata
---
## Goal
Use `new(std::align_val_t{...})` for over‑aligned types.
## Task
Define struct with `alignas(64)`; allocate with aligned new; delete with aligned delete.
## Acceptance
- [ ] Allocation aligns correctly; no leaks.