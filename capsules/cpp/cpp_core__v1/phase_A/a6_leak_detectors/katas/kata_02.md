---
title: A6/k2 — platform leak tool
kit_id: a6_leak_detectors
version: 1.0
status: Draft
type: kata
---
## Goal
Use a platform‑native detector to confirm the leak.
## Task
Windows: enable CRT leak check; Linux: valgrind `--leak-check=full`.
## Acceptance
- [ ] Native tool flags the same leak site.