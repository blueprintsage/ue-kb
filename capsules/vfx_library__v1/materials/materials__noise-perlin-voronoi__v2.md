# /materials/materials__noise-perlin-voronoi__v2.md
---
title: "Noise — Perlin & Voronoi (Unified)"
id: materials_noise-perlin-voronoi_v2
type: lesson
tags: ["lesson","materials","noise","perlin","voronoi","function","unified","remix:original"]
---
## Overview
Build two reusable noise functions—Perlin and Voronoi—and show practical masks for smoke, heat, shields, and decals without spaghetti graphs.
## Learning Goals
- Clean Material Functions (MF_Perlin, MF_Voronoi) with seed, scale, tiling.
- Combine/warp for breakup, masks, and motion without aliasing.
- Cheap preview material and instance presets.
## Prerequisites
Material function basics; understanding of UVs.
## Steps (outline)
1) **MF_Perlin** — Inputs: UV, Scale, Octaves, Seed; output 0–1; optional time panner.  
2) **MF_Voronoi** — Inputs: UV, Scale, Jitter; outputs: cells, edges, distance; mask edge with smoothstep.  
3) **Combinations** — Perlin→warp UV→Voronoi for organic edges; clamp and bias for mask use.  
4) **Use Cases** — Smoke alpha breakup, heat refraction mask, shield ripple mask, decal edge softening.  
5) **Preview** — Simple material to visualize noise; MI presets (Fine/Medium/Coarse).  
6) **Performance** — Prefer packed masks; cap octaves; animate via low-freq panners.
## Use Case: Crystalline Masks (Ice)
- Voronoi cells (distance) → edge mask (1 - smoothstep) → warp UV by Perlin (Scale 0.3–0.6).
- Bias to 0–1, then **clip** very thin lines (<0.05) to avoid shimmer at distance.
- Feed as opacity/emissive mask for frosty edges or impact cracks.
## Add-on Pack — Crystalline, Dark Veins
Crystalline: Voronoi edges warped by Perlin; clamp thin lines <0.05 to avoid shimmer.
Dark Veins (Shield): invert thin edge mask + slow warp; multiply subtly into opacity/emissive.
## Add-on Pack — Texture Authoring (Stylized)
Author at display scale (no micro-noise). Build crisp masks first, then add gentle warps.
Create 2–3 value steps max per mask; preview in grayscale and at Far LOD sizes.
Pack channels (R=mask, G=edge, B=warp seed, A=AO/height) to reduce lookups.
## QA Checklist
No visible tiling at gameplay distances; masks stay 0–1; animated noise doesn’t shimmer excessively.
## Release Notes
v2 — merged Perlin function + Voronoi variations into one card; added warp/mask recipes.
## Version notes
- Tested 5.1/5.3/5.4.  
- If Lumen shimmers with animated refraction masks, reduce panner speed or disable refraction on Low preset.
