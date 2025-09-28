---
title: BR01 — UMG HUD Basics
kit_id: br01_umg_hud_basics
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR01_UMG_Map
media:
- type: screenshot
views: [BEAUTY]
assets: []
dependencies: []
---


## Objective
Create a minimal HUD widget with a single progress bar bound to a Stamina float on the player; add it to the viewport on BeginPlay.


## Setup
- Project: UE5 BP project
- Map: `BR01_UMG_Map`


## Steps
1) Create `WBP_HUD` with a ProgressBar named `PB_Stamina`.
2) In Player BP, add `Stamina` (float, 0..1), default 0.5.
3) Bind `PB_Stamina.Percent` to Player `Stamina`.
4) On `BeginPlay`, `Create Widget(WBP_HUD)` → `Add to Viewport`.
5) Optional: Map input `IncreaseStamina`/`DecreaseStamina` to tweak ±0.1.


## Acceptance
- [ ] On PIE, bar shows 0.5 and updates when stamina changes.
- [ ] No lingering widget after level change.


## Keep/Revert
KEEP: Simple binding approach.
REVERT: Switch to Event-Driven binding if perf matters later.