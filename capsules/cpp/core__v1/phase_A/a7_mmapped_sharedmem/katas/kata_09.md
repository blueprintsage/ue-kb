---
title: A7/k9 — Windows MapViewOfFile
kit_id: a7_mmapped_sharedmem
version: 1.0
status: Draft
type: kata
---
## Goal
Provide a Windows implementation using `CreateFileMapping/MapViewOfFile`.
## Task
Guard with `#if _WIN32`; mirror API of POSIX wrapper.
## Acceptance
- [ ] Both POSIX and Win builds compile; tests green.