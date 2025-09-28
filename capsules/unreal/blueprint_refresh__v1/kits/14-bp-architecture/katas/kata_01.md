---
title: BR14/k1 — Interface call without cast
kit_id: br14_bp_arch
version: 1.0
status: Draft
type: kata
---
## Goal
Trigger Interact on door and pickup via interface.
## Task
Create BPI_Interact; Player calls `Interact()` on focused actor; remove all Cast nodes.
## Acceptance
- [ ] Both actors respond; zero Cast nodes remain.