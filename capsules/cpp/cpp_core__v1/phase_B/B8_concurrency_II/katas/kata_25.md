---
title: B8/k25 — Perf regression guard (p95 threshold)
kit_id: b8_perf_layout
version: 1.0
status: Draft
type: kata
---
## Objective
Fail CI if p95 exceeds baseline +10% on key benches.
## Acceptance
- [ ] Guard trips on injected slowdown; README explains updating baselines safely.
