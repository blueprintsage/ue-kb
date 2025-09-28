---
title: FX_<EmitterName> — Capture Playbook
kit_id: fx_<slug>
version: 1.0
status: Draft
category: VFX Niagara
deliverables:
demo_map: VFX_Capture_Map
media:
- type: screenshot
views: [TOP, SIDE, BEAUTY]
assets: []
dependencies: []
---


## Objective
Capture consistent diagnostic and beauty shots for this emitter.


## Setup
- Level: default or VFX_Capture_Map
- PostProcessVolume: Unbound, Manual Exposure (locked), Bloom OFF, Motion Blur 0
- CameraActors: Ortho_TOP, Ortho_SIDE, CineCam_BEAUTY


## Shots
1) **TOP** — frame full effect; include 1 m cube for scale.
2) **SIDE** — same.
3) **BEAUTY** — CineCam @ f/8–f/11.


## Capture
- Stills: `HighResShot 2`
- Clips (optional): MRQ 2–3 s @ 30 fps


## Acceptance
- [ ] 9 images saved under `/shots` with correct names.
- [ ] Exposure locked, Game View ON, naming matches.


## Keep/Revert
KEEP: Template OK.
REVERT: Adjust backgrounds as needed.