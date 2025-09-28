---
title: BR09 — Projectiles & Collisions
kit_id: br09_projectiles
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR09_Proj_Map
media:
- type: screenshot
views: [BEAUTY]
assets: []
dependencies: []
---


## Objective
Spawn a projectile with movement, detect hits, and broadcast impact data.


## Steps
1) BP_Projectile with `ProjectileMovement` (Speed 3000).
2) On Hit: stop, broadcast `OnImpact` (location/normal/actor).
3) Destroy after delay; expose damage as variable.


## Acceptance
- [ ] Hit fires once with correct impact data.
- [ ] No lingering projectiles.