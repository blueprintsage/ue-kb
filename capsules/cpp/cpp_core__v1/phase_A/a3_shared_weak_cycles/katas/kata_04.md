---
title: A3/k4 — shared_from_this pitfalls
kit_id: a3_shared_weak_cycles
version: 1.0
status: Draft
type: kata
---
## Goal
Use `enable_shared_from_this` correctly; avoid calling `shared_from_this()` before a `shared_ptr` owns the object.
## Task
Show failing case (stack/unique-owned object calling `shared_from_this` → throws/UB), then proper construction via `make_shared`.
## Acceptance
- [ ] Bad path detected/guarded; good path works and shares control block.