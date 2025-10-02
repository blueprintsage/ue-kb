---
title: B1/k15 — Deleted Functions to Block Misuse
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Use `= delete` to forbid illegal conversions or copying.
## Tasks
- Delete copy on noncopyable type; delete `operator==(char const*)` on string wrapper.
## Acceptance
- [ ] Misuse fails at compile‑time with clear diagnostics.