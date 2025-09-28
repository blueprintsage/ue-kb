---
title: A11/k2 — not_null invariants
kit_id: a11_implicit_mgmt_variants
version: 1.0
status: Draft
type: kata
---
## Goal
Prove not_null rejects null assignment.
## Task
Construct not_null<int*> from non-null; attempt nullptr (compile or runtime fail).
## Acceptance
- [ ] Null assignment prevented; valid path works.