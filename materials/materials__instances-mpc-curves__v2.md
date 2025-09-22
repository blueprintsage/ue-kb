# /materials/materials__instances-mpc-curves__v2.md
---
title: "Materials — Instances, MPC & Curves (Unified)"
id: materials_instances-mpc-curves_v2
type: lesson
tags: ["lesson","materials","instances","mpc","curves","workflow","unified","remix:original"]
---
## Overview
A practical workflow for tunable VFX: build a clean master material, make lightweight instances, expose global knobs with a Material Parameter Collection (MPC), and drive looks with curves.
## Learning Goals
- Master → Instance structure that stays readable.
- MPC for global color/intensity/lifetime; presets via curves.
- Safe hand-off to BP/Niagara without hard refs.
## Prerequisites
UE5 material basics; comfort with parameter naming.
## Steps (outline)
1) **Master Material** — Base inputs; scalar/vector params; switch(es) for optional features (e.g., refraction).  
2) **Instances** — Create MIs per effect (Core/Shell/Smoke); lock non-tunable params; name with `fx_*`.  
3) **MPC** — Make `MPC_Projectiles` (Color, Intensity, LifetimeBias); add getters in materials/MIs.  
4) **Curves** — Create Curve assets for Color/Intensity vs. distance or difficulty; sample from BP and push to MPC each tick or on state change.  
5) **Hooks** — From BP/Niagara, set MI params and MPC values; no asset hard refs in gameplay code—go through a router or soft refs.  
6) **Presets** — Low/Med/High via DataTable row → apply to MIs & MPC in one call.
## Recipe: Icy Fresnel & Refraction Mask
- **MF_IceRim:** Fresnel → pow → remap to 0–1 → multiply by blue-white tint; expose RimWidth/Intensity.
- **Mask:** MF_Voronoi (edges) warped by low-freq Perlin → smoothstep for crystalline breakup.
- **Refraction (optional):** mask * small scalar (0.01–0.03); gate with `bEnableRefraction`.
- **Instance setup:** M_IceCore (opaque) for shards; M_IceShell (translucent) for thin icicles.
- **MPC hooks:** `Ice_Intensity`, `Ice_Tint`, `Ice_RimWidth` for global grade tweaks.
- **Version notes:** 5.1–5.2 + Lumen → keep refraction low or off on Low preset.
## Add-on Pack — Color/Scale Presets, Shield/Ice Recipes
### Presets via DT
Low/Med/High rows with Color, Intensity, LifetimeBias; one Apply call sets MIs + MPC.
### Easy Scale/Color Control (AOE)
Expose `FX_Scale` (affects bounds, sizes, speeds) and `FX_Tint`; drive by DT/Curve; lock non-tunable params in MIs.
### Shield Material
Fresnel rim; scanline gate; optional tiny refraction; instances `MI_Shield_Shell/Core`; MPC keys `Shield_*`.
### Icy Fresnel & Mask
Fresnel rim × Voronoi-warped mask; optional refraction 0.01–0.03; `Ice_*` MPC keys.

## QA Checklist
Changes live-tweak in PIE; swapping presets doesn’t hitch; no circular refs; materials compile clean.
## Release Notes
v2 — merged “Instances — Tuning Workflow” with MPC/curves card; added preset pattern.
## Version notes
- Tested 5.1/5.3/5.4.  
- **Substrate**: prefer non-Substrate master for 5.1; if using Substrate (5.2+), keep a fallback MI and gate feature switches by quality.
