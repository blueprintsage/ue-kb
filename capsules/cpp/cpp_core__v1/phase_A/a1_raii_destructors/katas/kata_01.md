---
title: A1/k1 — FILE RAII wrapper
kit_id: a1_raii
version: 1.0
status: Draft
type: kata
---
## Goal
Wrap `FILE*` with automatic close on destruction.
## Task
`fopen`/`fclose` guarded by a class with move‑only semantics.
## Acceptance
- [ ] Read/write test passes; sanitizer shows no leaks.