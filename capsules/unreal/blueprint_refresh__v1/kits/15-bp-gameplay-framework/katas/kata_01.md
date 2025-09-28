---
title: BR15/k1 — Two-player PIE state sync
kit_id: br15_bp_framework
version: 1.0
status: Draft
type: kata
---
## Goal
Ensure GameState/PlayerState hold the right data across two players.
## Task
Run 2-player PIE; update score in GameMode; verify UI reads from GameState for both clients.
## Acceptance
- [ ] Both clients display the same score/time.