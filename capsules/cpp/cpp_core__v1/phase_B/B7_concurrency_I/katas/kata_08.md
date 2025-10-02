---
title: B7/k8 — Deterministic builds (SOURCE_DATE_EPOCH)
kit_id: b7_build_tooling
version: 1.0
status: Draft
type: kata
---
## Objective
Strip non-determinism (timestamps, paths) from artifacts.
## Acceptance
- [ ] Two builds with same inputs hash-identical; build logs note deterministic mode.
