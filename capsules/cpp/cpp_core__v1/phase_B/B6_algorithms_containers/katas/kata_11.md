---
title: B6/k11 — Panic boundary & fail-fast policy
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Define a panic handler for “should never happen” cases with minimal crash report.
## Acceptance
- [ ] Panic emits one structured line (JSONL) and terminates; test catches via death test.
