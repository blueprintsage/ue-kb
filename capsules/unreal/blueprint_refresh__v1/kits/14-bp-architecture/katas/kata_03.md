---
title: BR14/k3 — Focus trace → interface call
kit_id: br14_bp_arch
version: 1.0
status: Draft
type: kata
---
## Goal
Interact with any implementer without casts.
## Task
Line trace from view; if hit implements BPI_Interact → call Interact.
## Acceptance
- [ ] Works on two different actor types with zero Cast nodes.