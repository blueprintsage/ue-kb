---
title: BR07/k3 — Clamp & edge-case guards
kit_id: br07_hud_meters
version: 1.0
status: Draft
type: kata
---
## Goal
Prevent invalid HUD values.
## Task
Clamp all stats to 0..1 (or 0..Max) on set; guard AmmoMax>0; hide bar at 0 if desired.
## Acceptance
- [ ] No NaN/inf; Ammo/AmmoMax never divide-by-zero; UI never shows <0 or >1.