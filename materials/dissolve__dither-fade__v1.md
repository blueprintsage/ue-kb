---
id: materials__dissolve__dither-fade__v1
family: materials
topic: dissolve__dither-fade
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
tags: ["dissolve","dither","fade","series:sci-fi-vfx","part:3","source:book:butler"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Dissolve / Dither Fade


## Summary
Clean thresholds with a packed mask and TAA‑friendly dithered opacity.


## Recipe
- Pack noise into blue channel; single compare for branchless cut.
- Rim from `smoothstep(threshold ± width)` → emissive.
- Prefer `DitherTemporalAA` over hard alpha clip.