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
## Optional: Frost Overlay (Screen/Camera Hit)
- **Goal:** brief frosty rim on the camera during heavy ice impacts without obscuring gameplay.
- **Material:** Post-process blendable (Before Tonemapping). Use the **crystalline mask** (Voronoi warped by Perlin) → multiply by a radial gradient from screen center or impact direction. Output to **EmissiveColor** (subtle blue-white) and a faint **Bloom** contribution; keep **Opacity** very low (0.05–0.12).
- **Trigger (BP):** On strong impact, add blendable to PP Volume with `Weight = 1.0` → timeline to fade to `0` in **0.25–0.4 s**; cooldown 1–2 s to avoid stacking.
- **Performance/Comfort:** Clamp max intensity on Low preset; disable if motion blur is high or in photo-sensitive mode.
- **Version notes:** Works 5.1–5.4. If color shifts in MRQ (5.1), use **Cinematic** preset and lock exposure.
## Add-on Pack — Bullet/Scorch, Water/Blood, Frost, Shield Ground Glow

### Bullet Impact Decal
Soft circular mask; 6–14 cm; rotate from normal/tangent; life 8–30 s (game) or 0.8–1.5 s (cinematic scorch).
### Scorch / Burn Mark
DBuffer decal with subtle normal dent + dark ring; size 20–60 cm; atlas variants; smooth fade.
### Wet Splash (Water)
Radial ring, very low roughness + darker albedo; life 0.6–2.0 s; disable on Low.
### Blood Splatter
Albedo only, no normals; small cluster atlas; splat angle from surface tangent; life 30–120 s or pooled; comfort: clamp saturation.
### Frost Overlay (Camera)
Post-process blendable; crystalline mask × radial gradient; emissive subtle; fade 0.25–0.4 s; cooldown 1–2 s.
### Shield Ground Glow
Unlit radial glyph; life 0.8–1.2 s; rotate from facing; disable on Low.


## QA Checklist
No z-fighting; no stretched UVs on steep angles; fade is smooth; pooled decals never exceed cap; perf stable in overdraw view.
## Release Notes
v2 — merged “Impact Decals — Spawn on Hit” + “Impact Decals — Polish”, added router + pooling notes.
## Version notes
- Tested 5.1/5.3/5.4.  
- 5.1–5.2 DBuffer quirks: if normals don’t show, confirm Project Settings → Rendering → **Decals** DBuffer is enabled; recompile shaders.  
- Lumen shimmer: keep Emissive modest or gate via quality preset on Low.
