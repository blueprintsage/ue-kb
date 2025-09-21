---
id: materials__hologram__scanline-dither__v1
family: materials
topic: hologram__scanline-dither
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
source: []
tags: ["hologram","dither","scanline","series:sci-fi-vfx","part:2"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Hologram — Scanline & Dither


## Summary
Hologram look with scrolling scanlines, depth‑aware fade, and TAA‑friendly dithered opacity.


## Walkthrough
1. Parent `M_Hologram`: Unlit; vertical scanline (sine + panner) combined with base color.
2. Multiply by a scene/object depth factor to reduce background bleed.
3. Use `DitherTemporalAA` before opacity for clean fades.
4. Params: `LineDensity`, `Speed`, `Color`, `OpacityMin`.


## QA
Check readability on bright/dark backgrounds; clamp opacity to avoid TAA ghosts.


---
## Sci‑Fi Batch 1 — Part 2 Additions (2025‑09‑21)
- Added depth modulation and dither step; standardized exposed params.