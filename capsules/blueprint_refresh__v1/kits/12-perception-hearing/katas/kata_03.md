---
title: BR12/k3 — Hearing-driven investigate flow
kit_id: br12_perception_hearing
version: 1.0
status: Draft
type: kata
---
## Goal
Use hearing to drive investigate, then fall back to patrol.
## Task
On perceive noise: set `LastKnownLocation` and switch to investigate subtree; clear after wait.
## Acceptance
- [ ] Clean return to patrol after timeout.