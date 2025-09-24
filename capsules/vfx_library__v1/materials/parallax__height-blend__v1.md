---
id: materials__parallax__height-blend__v1
family: materials
topic: parallax__height-blend
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
tags: ["parallax","heightlerp","series:sci-fi-vfx","part:3","source:book:butler"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Parallax & Height‑Blend (Ground/Decals)


## Summary
Stable height‑based blending for ground decals and materials.


## Steps
- Remap height maps to 0..1 before lerp; expose `HeightContrast` for art.
- Cap parallax steps; beyond 20m switch to cheaper height blend.
## Add-on Pack — Related & Cross‑Link
See also: **Parallax Occlusion Mapping** → `materials/parallax__occlusion-mapping__v1.md`.
Clarify: Height‑Blend for ground/decals; POM for close, hero surfaces; both fade by distance.

## QA
Grazing angles; decals on uneven terrain.