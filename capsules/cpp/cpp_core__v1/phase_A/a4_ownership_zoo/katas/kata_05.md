---
title: A4/k5 — move owner into setter/factory
kit_id: a4_ownership_zoo
version: 1.0
status: Draft
type: kata
---
## Goal
Accept/return owners by value to make ownership explicit.
## Task
`set_resource(std::unique_ptr<R> r)` and `make_resource() -> std::unique_ptr<R>`; tests ensure callers move/receive as owners.
## Acceptance
- [ ] Compile errors if caller tries to copy; moves succeed.