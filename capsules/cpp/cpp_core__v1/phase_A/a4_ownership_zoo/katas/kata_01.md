---
title: A4/k1 — reference vs pointer observer
kit_id: a4_ownership_zoo
version: 1.0
status: Draft
type: kata
---
## Goal
Choose reference (required) vs pointer (optional) for non‑owning access.
## Task
Write two funcs: `tick(Widget& required)` and `maybe_tick(Widget* optional)`; prove required cannot be null and optional path guards null.
## Acceptance
- [ ] Tests compile and pass; null only allowed in pointer case.