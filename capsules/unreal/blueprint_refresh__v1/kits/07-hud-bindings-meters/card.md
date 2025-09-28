---
title: BR07 — HUD Bindings & Meters
kit_id: br07_hud_meters
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR07_UMG_Map
media:
- type: screenshot
views: [BEAUTY]
assets: []
dependencies: [br01_umg_hud_basics]
---


## Objective
Bind multiple UMG meters (Health/Stamina/Ammo) to player variables with safe updates.


## Steps
1) Add bars `PB_Health`, `PB_Stamina`, `PB_Ammo` to `WBP_HUD`.
2) Expose player floats; clamp 0..1 on set.
3) Create `OnChanged` dispatcher or event-driven updates to avoid Tick.


## Acceptance
- [ ] All bars update without Tick-based bindings.
- [ ] No out-of-range values displayed.