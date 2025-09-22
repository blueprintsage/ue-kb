---
id: materials__decals__impact-polish__v1
family: materials
topic: decals__impact-polish
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
tags: ["decal","impact","polish","series:sci-fi-vfx","part:3","source:book:butler"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Impact Decals — Polish


## Summary
Cleaner projections and consistent lifespans for hits, scorch, and stains.


## Settings
- Small negative depth bias to prevent z‑fight (clamped to avoid light leaks).
- Use Translucent for emissive flashes; DBuffer Translucent Color for persistent stains.


## Lifespan Bins
- Sparks **0.5s**, Scorch **3s**, Stain **30s** — use separate MIs.


## QA
Test on high‑metallic and extremes of roughness.