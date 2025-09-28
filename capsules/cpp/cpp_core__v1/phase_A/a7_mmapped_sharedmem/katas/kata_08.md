---
title: A7/k8 — alignment & span<T>
kit_id: a7_mmapped_sharedmem
version: 1.0
status: Draft
type: kata
---
## Goal
Validate alignment before casting to `span<T>`.
## Task
Check `std::align`/pointer mod; fall back to `std::byte` if misaligned.
## Acceptance
- [ ] No UB; tests pass with odd offsets.