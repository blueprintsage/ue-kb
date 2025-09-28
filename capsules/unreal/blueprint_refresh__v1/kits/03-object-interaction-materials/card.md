---
title: BR03 — Object Interaction & Material Swaps
kit_id: br03_object_interaction
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR03_Interact_Map
media:
- type: screenshot
views: [BEAUTY]
assets: []
dependencies: []
---


## Objective
Enable player to interact with an actor to toggle a highlight material instance and play a sound.


## Setup
- Create `MI_Highlight` from a base material with a scalar `Glow`.


## Steps
1) Add a `Sphere` trigger to the actor; on overlap, show on-screen prompt.
2) On `E` pressed while overlapping, toggle a `Glow` scalar on a MID.
3) Optional: play a `Click` sound and spawn a small Niagara spark.


## Acceptance
- [ ] Material toggles reliably; prompt appears only in range.
- [ ] No MID leaks (reuse created MID).


## Keep/Revert
KEEP: Single MID reused.
REVERT: Switch to Dynamic Material on specific element if multi-mesh.