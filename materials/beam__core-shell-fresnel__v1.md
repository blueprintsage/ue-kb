---
id: materials__beam__core-shell-fresnel__v1
family: materials
topic: beam__core-shell-fresnel
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
source: []
tags: ["beam","fresnel","emissive","series:sci-fi-vfx","part:2"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Beam Material — Core/Shell Fresnel


## Summary
Reusable two‑layer beam material: a tight **core** for brightness and a softer **shell** for volume, driven by Fresnel. Suitable for lightning arcs, rail beams, and scanner lines.


## Setup
- Create `M_Beam_CoreShell` (Shading Model: Unlit).
- Textures: optional thin ramp (core), subtle noise/normal map (shell/distortion).


## Walkthrough
1. **Core:** UV ramp → multiply by `CoreWidth` → clamp → `EmissiveColor` * `CoreGlow`.
2. **Shell:** `Fresnel` → `Pow(ShellPower)` → color via param/vector → add to emissive.
3. **Optional Distortion:** normal map → slow `Panner` → plug small value into Refraction (keep tiny).
4. Expose params: `CoreWidth`, `CoreGlow`, `ShellWidth`, `ShellPower`, `Color`, `NoiseAmount`.
5. Author `MI_Beam_*` instances (thin/medium/thick) for quick reuse.


## Performance
- Clamp emissive to avoid bloom smears; avoid high refraction cost.
- Check mip bias on thin lines so they hold up at distance.


## QA
- No extreme WPO; preview at multiple FOVs and TAA.


---
## Sci‑Fi Batch 1 — Part 2 Additions (2025‑09‑21)
- Clarified core/shell roles, added minimal refraction guidance, and standardized preset params.