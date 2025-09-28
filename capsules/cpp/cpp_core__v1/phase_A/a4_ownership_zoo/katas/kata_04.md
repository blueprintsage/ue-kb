---
title: A4/k4 — duplicate handle wrapper
kit_id: a4_ownership_zoo
version: 1.0
status: Draft
type: kata
---
## Goal
Wrap an OS handle (int fd or FILE*) in RAII that supports `dup()` semantics.
## Task
Implement `handle` with `close()` in dtor; disabled copy; add `dup_handle()` creating a new independent owner.
## Acceptance
- [ ] Each handle closes exactly once; no double‑close under ASan.