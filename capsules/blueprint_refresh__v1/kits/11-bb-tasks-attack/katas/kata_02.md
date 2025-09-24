---
title: BR11/k2 — Cooldown logic guard
kit_id: br11_bb_attack_investigate
version: 1.0
status: Draft
type: kata
---
## Goal
Prevent attack spam.
## Task
Use DoOnce or Gate with a Reset by timer; log first-then-block pattern.
## Acceptance
- [ ] Attacks obey cooldown across target jitter.