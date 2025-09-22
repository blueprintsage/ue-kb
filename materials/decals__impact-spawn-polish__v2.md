# /materials/decals__impact-spawn-polish__v2.md
---
title: "Impact Decals — Spawn & Polish (Unified)"
id: decals_impact-spawn-polish_v2
type: lesson
tags: ["lesson","materials","decal","impact","bp","polish","unified","remix:original"]
---
## Overview
Single stop for impact decals: fast spawn from gameplay/FX events, clean material setup (normal/roughness/emissive optional), and polish that avoids z-fighting, stretching, and pop-out fades.
## Learning Goals
- Build a flexible impact decal MI (albedo/normal/roughness, soft mask, optional emissive).
- Spawn routes: BP line trace, Niagara collision event, and Router DT row.
- Lifespan/fade tuning; surface-aligned projection; atlas-friendly UVs.
## Prerequisites
Basic materials, BP traces/events, and one working hit event (from your project or the Hit Impact card).
## Steps (outline)
1) **Material**: DBuffer-enabled decal → soft circular mask → normal & roughness slots; optional emissive pulse.  
2) **MI Params**: BaseColorTint, NormalStrength, Roughness, Emissive, FadeStart/End, SizeXY.  
3) **Spawn**:  
   - BP: LineTrace → BreakHitResult → `SpawnDecalAtLocation` with Size/Rotation from `ImpactNormal`.  
   - Niagara: Collision → `Send To Router` (tag: `FX.Impact.Decal`) → BP router spawns decal.  
4) **Polish**: Nudge off-surface (tiny offset), clamp extreme angles, depth bias if needed.  
5) **Cleanup**: Timed fade (<1.2s), optional decal pool (N preallocated comps).
## QA Checklist
No z-fighting; no stretched UVs on steep angles; fade is smooth; pooled decals never exceed cap; perf stable in overdraw view.
## Release Notes
v2 — merged “Impact Decals — Spawn on Hit” + “Impact Decals — Polish”, added router + pooling notes.
## Version notes
- Tested 5.1/5.3/5.4.  
- 5.1–5.2 DBuffer quirks: if normals don’t show, confirm Project Settings → Rendering → **Decals** DBuffer is enabled; recompile shaders.  
- Lumen shimmer: keep Emissive modest or gate via quality preset on Low.
