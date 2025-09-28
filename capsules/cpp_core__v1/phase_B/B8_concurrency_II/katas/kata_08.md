---
title: B8/k8 — Inlining & hot/cold function splits
kit_id: b8_perf_layout
version: 1.0
status: Draft
type: kata
---
## Objective
Isolate cold error paths; encourage inlining on hot path.
## Acceptance
- [ ] Hot path faster after split; code size measured; no perf regressions on cold.
