# /niagara/portal__rim-outline-polish__v2.md
---
title: "Portal — Rim Outline & Polish (Unified)"
id: portal_rim-outline-polish_v2
type: lesson
tags: ["lesson","niagara","portal","rim","depthfade","spark-layer","unified","remix:original"]
---
## Overview
Build a clean, stylized portal rim: fresnel/edge width you can read from distance, soft intersections via DepthFade, and a light spark layer—shippable and easy to retune.
## Learning Goals
- Rim material with **Fresnel + thickness control**, optional refraction guard.
- Niagara outline using **Shape Location (surface-only)** and stable bounds.
- Spark/ember secondary that doesn’t overwhelm the rim read.
## Prerequisites
First VFX material; shape location basics.
## Steps (outline)
1) **Material (Rim)** — Fresnel → pow → bias for controllable rim width; optional **Refraction** (gate via bool param); add tint/intensity controls.  
2) **Intersection** — Add **DepthFade**; test at glancing angles; clamp fade distance for thin geometry.  
3) **Niagara Outline** — Emitter: **Shape Location: Mesh (surface-only)** → inherit normals; size over life for swell-in; fix **System Fixed Bounds**.  
4) **Spark Layer** — Ribbon or sprite secondary with low spawn; random bursts; color slightly offset; lifetime < 0.4s.  
5) **Polish** — Camera-distance bias for rim width; reduce spark rate when player is far; ensure portal read in unlit view as a sanity check.
## QA Checklist
Rim stays readable at 10/25/40m; no harsh intersections; spark layer never clips over the rim; bounds don’t cull at camera edges.
## Release Notes
v2 — merged “Rim Outline” + “Outline Polish”; added surface-only shape setup and spark recipe.
## Version notes
- Tested 5.1/5.3/5.4.  
- If refraction shimmers (5.1–5.2 + Lumen): disable refraction or gate via quality preset.  
- Shape Location: ensure **Surface Only** checked; if particles leak, tighten source mesh normals or bias spawn offset inward.
