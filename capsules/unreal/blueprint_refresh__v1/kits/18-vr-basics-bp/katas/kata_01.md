---
title: BR18/k1 — Controller trace & grab interface
kit_id: br18_vr_basics
version: 1.0
status: Draft
type: kata
---
## Goal
Line/sphere trace from motion controller and grab actors via interface.
## Task
Implement `BPI_Grabbable`; on trigger, trace → call `Grab/Release`.
## Acceptance
- [ ] Can grab and release a cube reliably in VR Preview.