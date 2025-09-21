---
id: niagara__teleport__disintegrate-reintegrate__v1
family: niagara
topic: teleport__disintegrate-reintegrate
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
source: []
tags: ["teleport","mesh-particles","dither","series:sci-fi-vfx","part:2"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Teleport — Disintegrate/Reintegrate (Niagara)


## Summary
Character dissolves into mesh particles at the source and reforms at the destination, synced to BP events.


## System
- Emitter A (disintegrate): Mesh particles sampled from the source mesh; outward velocity; noise‑threshold dissolve.
- Emitter B (reintegrate): Attraction toward target transform; fade in; align to normals.
- Material: dithered opacity + emissive edge pulse; color from user param.


## BP Hooks
- Timeline drives dissolve thresholds; disables collision during disintegration; teleports at zero‑mass state.


## QA
Use fixed tick for cinematic consistency; verify collisions off during the effect.


---
## Sci‑Fi Batch 1 — Part 2 Additions (2025‑09‑21)
- Added mesh‑particle method, BP sync notes, and safety toggles.