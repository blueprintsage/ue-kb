---
title: A6/k1 — asan/lsan leak
kit_id: a6_leak_detectors
version: 1.0
status: Draft
type: kata
---
## Goal
Trigger a simple leak and read the sanitizer report.
## Task
`auto p = new int[16]; (void)p;` without delete; run tests under `-fsanitize=address,leak`.
## Acceptance
- [ ] Report shows 16*sizeof(int) bytes leaked with stack trace.