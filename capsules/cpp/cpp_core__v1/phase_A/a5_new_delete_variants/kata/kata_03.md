---
title: A5/k3 — exception safety make_unique
kit_id: a5_new_delete_variants
version: 1.0
status: Draft
type: kata
---
## Goal
Prefer factory helpers for exception safety.
## Task
Throw in constructor of T; compare `new T` vs `make_unique<T>` for leak safety.
## Acceptance
- [ ] `make_unique` version leaks nothing; raw `new` leaks.