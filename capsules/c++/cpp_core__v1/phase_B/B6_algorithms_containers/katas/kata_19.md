---
title: B6/k19 — Logging context propagation with errors
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Attach `trace_id`/`run_id` context to errors and propagate across layers.
## Acceptance
- [ ] Error printed at the top includes originating `trace_id`; intermediate layers add breadcrumbs without losing the original code.
