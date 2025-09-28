---
title: A5/k1 — new vs new[] mismatch
kit_id: a5_new_delete_variants
version: 1.0
status: Draft
type: kata
---
## Goal
Show UB when `new[]` memory is freed with plain `delete`.
## Task
Allocate `new int[3]`, delete with `delete`; run under ASan.
## Acceptance
- [ ] ASan reports invalid free.