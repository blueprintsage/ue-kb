---
title: BR07/k1 — Event-driven HUD bindings (no Tick)
kit_id: br07_hud_meters
version: 1.0
status: Draft
type: kata
---
## Goal
Update HUD bars via events instead of Tick bindings.
## Given
Player variables: Health, Stamina, Ammo (floats 0..1). WBP_HUD with three bars.
## Task
Create a `OnStatsChanged` dispatcher on Player; on var change, broadcast and update widget via a bound event.
## Acceptance
- [ ] Bars reflect changes immediately; no Tick used.
- [ ] Changing any stat fires exactly one update.