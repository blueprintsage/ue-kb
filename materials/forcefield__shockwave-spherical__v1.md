---
id: niagara__forcefield__shockwave-spherical__v1
family: niagara
topic: forcefield__shockwave-spherical
version: 1
ue: ["5.3","5.4","5.5"]
status: draft
license: GPL-3.0-or-later
art_license: CC-BY
tags: ["shockwave","sphere","refraction","series:sci-fi-vfx","part:2"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Forcefield — Spherical Shockwave (Niagara)


## Summary
Expanding spherical shockwave with refraction ring and dust motes.


## Walkthrough (generic)
- Emitter A: expanding ring (quad); animate UVs for ripples; use refraction material lightly.
- Emitter B: sparse GPU sprites pushed by outward force for dust.
- Expose duration/radius curves for timing control.


## QA
Keep refraction under perf budget; ensure far bounds for large waves.