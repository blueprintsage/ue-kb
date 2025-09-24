---
id: niagara__forcefield__shockwave-spherical__v1
family: niagara
topic: forcefield__shockwave-spherical
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
source: []
tags: ["shockwave","sphere","refraction","series:sci-fi-vfx","part:2"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Forcefield — Spherical Shockwave (Niagara)


## Summary
Expanding spherical shockwave with a subtle refraction ring and sparse dust motes.


## System
- Emitter A: expanding quad ring; ripple UVs for concentric waves; uses a lightweight refraction material.
- Emitter B: GPU sprites pushed outward by a radial force for dust.
- Exposed curves: `RadiusOverTime`, `OpacityOverTime`, `DustDensity`.


## QA
Ensure large bounds for big waves; track refraction cost in shader complexity.


---
## Sci‑Fi Batch 1 — Part 2 Additions (2025‑09‑21)
- Added dust motes and curve‑driven timing; refined refraction budget note.