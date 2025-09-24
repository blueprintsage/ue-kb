---
title: BR13/k3 — DoOnce/Gate spam guard
kit_id: br13_adv_nodes
version: 1.0
status: Draft
type: kata
---
## Goal
Stop repeated events from flooding logic.
## Task
Wrap expensive section in DoOnce with timed Reset or Gate Open/Close.
## Acceptance
- [ ] Only first event within window executes.