---
title: D2/k4 — Observer tokens
kit_id: d2_command_events_observer
version: 1.0
status: Draft
type: kata
---
## Goal
Safe subscribe/unsubscribe with lifetime management.
## Task
Emit events; subscriber auto‑unsubscribes on token dtor; no dangling calls.
## Acceptance
- [ ] No calls after unsubscribe; tests pass under sanitizer.