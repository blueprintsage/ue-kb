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
## QA Checklist
No visible tiling at gameplay distances; masks stay 0–1; animated noise doesn’t shimmer excessively.
## Release Notes
v2 — merged Perlin function + Voronoi variations into one card; added warp/mask recipes.
## Version notes
- Tested 5.1/5.3/5.4.  
- If Lumen shimmers with animated refraction masks, reduce panner speed or disable refraction on Low preset.
