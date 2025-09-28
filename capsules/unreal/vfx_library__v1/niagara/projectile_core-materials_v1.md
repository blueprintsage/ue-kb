# /niagara/projectile__core-materials__v1.md
---
title: "Projectile — Core Materials"
id: projectile_core-materials_v1
type: lesson
tags: ["lesson","niagara","materials","projectile","remix:original"]
---
## Overview
Author a readable projectile core with core/shell emissive, fresnel rim, and optional distortion—built as reusable material functions.
## Learning Goals
- Core→shell layering with tunable brightness and radius.
- Param sweep that holds shape from 5–30m and in motion blur.
## Prerequisites
UE5 materials basics; Niagara familiarity.
## Steps (outline)
MF_CoreGlow → MF_ShellFresnel → combine in M_ProjectileCore → MI variants; expose Color/Intensity/Radius.
## Add-on: Projectile Core/Shell (Electric & Magic)
- **Core:** tight emissive band; optional BlackBody bias for hot variants.
- **Shell (electric):** fresnel rim + crackle mask (Perlin-warped Voronoi); clamp emissive by distance.
- **Alpha modes:** Additive for beams/magic, AlphaComposite for thicker orbs; Substrate fallback OFF for 5.1.
- **Params:** `FX_Color`, `FX_Intensity`, `FX_RimWidth`, `FX_NoiseScale` (MIs) + MPC mirrors for presets.

## QA Checklist
No overbright clipping; refraction optional/off on low preset; LODs stable.
## Release Notes
v1.0 — first pass functions + instance setup.
