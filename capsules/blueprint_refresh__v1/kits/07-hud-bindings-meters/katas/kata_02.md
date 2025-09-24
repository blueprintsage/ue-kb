---
title: BR07/k2 — Ammo text + bar dual binding
kit_id: br07_hud_meters
version: 1.0
status: Draft
type: kata
---
## Goal
Show Ammo as both a bar (0..1) and a text counter.
## Given
Player ints: Ammo, AmmoMax; WBP_HUD has PB_Ammo and TXT_Ammo.
## Task
Bind PB_Ammo.Percent = Ammo / AmmoMax; bind TXT_Ammo to "Ammo/AmmoMax".
## Acceptance
- [ ] Both bar and text update together without Tick.