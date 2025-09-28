---
title: BR14 — Blueprint Architecture (Components/Interfaces)
kit_id: br14_bp_arch
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR14_Arch_Map
media:
- type: screenshot
views: [BEAUTY]
assets: []
dependencies: []
---


## Objective
Compose actors using components and decouple interactions using Blueprint Interfaces.


## Steps
1) Add a **HealthComponent** to handle damage/regen.
2) Create **BPI_Interact** with `Interact()`; implement on a door and a pickup.
3) Player calls `Interact()` on focused actor via interface, not concrete type.


## Acceptance
- [ ] Door and pickup both respond to Interact without casts.
- [ ] HealthComponent usable on multiple actors.