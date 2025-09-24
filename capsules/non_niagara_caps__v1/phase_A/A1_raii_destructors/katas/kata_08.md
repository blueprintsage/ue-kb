---
title: A1/k8 — double‑free defense
kit_id: a1_raii
version: 1.0
status: Draft
type: kata
---
## Goal
Design state to prevent double‑free on moved‑from objects.
## Task
Sentinel nulling + idempotent deleter.
## Acceptance
- [ ] Tests show no double‑free under repeated destroy.