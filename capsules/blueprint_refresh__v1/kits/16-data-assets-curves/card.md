---
title: BR16 — Data Assets/Curves in BP
kit_id: br16_data_curves
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR16_Data_Map
media:
- type: screenshot
views: [BEAUTY]
assets: []
dependencies: []
---


## Objective
Parameterize gameplay using **Primary Data Assets** and **Curve** assets for tuning.


## Steps
1) Create DataAsset `DA_Weapon` (Damage, Rate, Spread).
2) Create CurveFloat `CF_Recoil`; sample over time in BP.
3) Player reads DataAsset values; applies Curve to recoil each shot.


## Acceptance
- [ ] Changing DataAsset or Curve updates behavior without BP edits.
- [ ] No hard-coded constants remain in logic.