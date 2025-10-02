---
title: B12/k16 — Fuzz critical parser/loader
kit_id: b12_capstone
version: 1.0
status: Draft
type: kata
---
## Objective
Attach a fuzz target to a minimal parser or config loader.
## Acceptance
- [ ] 1K random inputs hit no crashes/UB; any failure reports a reproducible seed and shrunk input.
