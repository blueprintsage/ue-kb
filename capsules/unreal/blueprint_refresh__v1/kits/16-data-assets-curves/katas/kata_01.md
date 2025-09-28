---
title: BR16/k1 — Swap DataAssets at runtime
kit_id: br16_data_curves
version: 1.0
status: Draft
type: kata
---
## Goal
Hot-swap a weapon DataAsset to change behavior.
## Task
Expose `CurrentWeapon` DataAsset; change it via key; behavior (damage/rate) updates.
## Acceptance
- [ ] Swapping asset changes behavior without BP edits.