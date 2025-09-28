---
id: niagara__teleport__disintegrate-reintegrate__v1
family: niagara
topic: teleport__disintegrate-reintegrate
version: 1
ue: ["5.3","5.4","5.5"]
status: draft
license: GPL-3.0-or-later
art_license: CC-BY
tags: ["teleport","mesh-particles","dither","series:sci-fi-vfx","part:2"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Teleport — Disintegrate/Reintegrate (Niagara)


## Summary
Character teleports by dissolving into mesh particles and reforming at the destination.


## Walkthrough (generic)
1) Source: mesh particles from character mesh; sample vertex color/UVs for spawn timing.
2) Drive dissolve with noise threshold; add velocity outward → then inward at target.
3) Material uses dithered fade + emissive edge; sync with BP timeline.


## QA
Fixed tick for cinematic consistency; ensure collision disabled during disintegration.