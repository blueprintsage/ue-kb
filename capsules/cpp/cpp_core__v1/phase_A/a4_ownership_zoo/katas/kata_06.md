---
title: A4/k6 — container of unique_ptr
kit_id: a4_ownership_zoo
version: 1.0
status: Draft
type: kata
---
## Goal
Store owners in `std::vector<std::unique_ptr<T>>` and iterate observers.
## Task
Push_back via `std::make_unique`; iterate and call method via observers.
## Acceptance
- [ ] No copies of T or unique_ptr; behavior correct.