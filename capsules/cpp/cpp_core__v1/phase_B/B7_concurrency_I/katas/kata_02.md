---
title: B7/k2 — Treat warnings as errors (per target)
kit_id: b7_build_tooling
version: 1.0
status: Draft
type: kata
---
## Objective
Flip `-Werror`/`/WX` only for project libraries/apps, not tests or externals.
## Acceptance
- [ ] Intentional warning fails the target build; tests/external deps still compile.
