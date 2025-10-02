---
title: D2/k3 — Event queue budget
kit_id: d2_command_events_observer
version: 1.0
status: Draft
type: kata
---
## Goal
Only process up to K events per frame.
## Task
Queue N>>K; run frames; verify carry‑over and completion.
## Acceptance
- [ ] No starvation; all events processed.