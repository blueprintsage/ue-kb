---
title: BR18 — VR Basics (BP)
kit_id: br18_vr_basics
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR18_VR_Map
media:
- type: screenshot
views: [BEAUTY]
assets: []
dependencies: []
---


## Objective
Set up a simple VR pawn with motion controllers and grab interaction.


## Steps
1) Enable VR plugin; use VR template pawn or create MotionController components.
2) Add line/sphere trace from controller; implement grab/release interface.
3) Teleport locomotion with NavMesh and arc trace.


## Acceptance
- [ ] Grab/release works; teleport respects NavMesh.
- [ ] Controllers visible/tracked in PIE (VR Preview).