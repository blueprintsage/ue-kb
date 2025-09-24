# /niagara/flipbook__smoke-subuv-depthfade__v2.md
---
title: "Flipbook — Smoke + SubUV + DepthFade (Unified)"
id: flipbook_smoke-subuv-depthfade_v2
type: lesson
tags: ["lesson","niagara","flipbook","subuv","depthfade","sprite","unified","remix:original"]
---
## Overview
One stop for sprite flipbooks: smoke setup, Sub-UV animation, and DepthFade for clean intersections—plus a rocket-smoke preset.
## Learning Goals
- Author a Sub-UV material with life-linear blending.
- Use DepthFade to avoid hard cuts at geometry.
- Tune curves (size/color/alpha) for readability at 5/15/30m.
## Prerequisites
Niagara sprite basics; first VFX material.
## Steps (outline)
Texture import & packing → M_Smoke_SubUV (life-linear) → DepthFade node & range test → Niagara sprite emitter with size/color/alpha over life → preview & bounds → **Preset: Rocket Smoke** (lower contrast, shorter life, distance fade).
## Preset: Cold Smoke
- Flipbook frames with **less orange, more neutral/blue**; Life 0.3–0.7 s for quick frost bursts.
- DepthFade shorter (20–35 cm) to avoid haloing on thin geometry.
- Color over life: blue-gray → desaturate; alpha over life eases out (no hard cut).
## Add-on Pack — Smoke/Steam, Dust, Liquids
### Steam Column (Beginner)
Spawn small radius, upward vel 150–250 cm/s + light Drag; 12–16f flipbook, life-linear blend; DepthFade 25–40 cm; Size ↑ over life, warm→cool gray, Alpha ease-out; lifetime 1.2–2.0 s; tiny Curl Noise wobble.
### Rotor Wash / Landing Dust
Ring burst + low cloud; outward radial + slight lift; low-contrast sheet; DepthFade 15–25 cm; fixed bounds = landing radius ×1.2.
### Cold Smoke (Ice)
Cool palette; life 0.3–0.7 s; short DepthFade 20–35 cm; gentle alpha out.
### Water Mist / Splash Puff
Short life 0.15–0.35 s; darker base → quick fade; soften intersections aggressively (DepthFade 30–50 cm); prefer fewer, larger sprites.
### Fog (Ground)
Very low contrast; scale by distance to camera; lifetime 2–6 s; disable secondaries at Far LOD.
### Dust Storm Sheets
Wide sprites with low-freq panners; random per-emitter UV off; clip bright albedo to avoid banding.
## Add-on Pack — Smoke/Steam, Dust, Liquids
### Steam Column (Beginner)
Spawn small radius; upward vel 150–250 cm/s + light Drag; 12–16f flipbook (life-linear); DepthFade 25–40 cm; Size ↑ over life; warm→cool gray; Alpha ease-out; lifetime 1.2–2.0 s; tiny Curl Noise wobble.
### Rotor Wash / Landing Dust
Ring burst + low cloud; outward radial + slight lift; low-contrast sheet; DepthFade 15–25 cm; fixed bounds = landing radius ×1.2.
### Cold Smoke (Ice)
Cool palette; life 0.3–0.7 s; DepthFade 20–35 cm; gentle alpha out.
### Water Mist / Splash Puff
Life 0.15–0.35 s; darker base → quick fade; DepthFade 30–50 cm; prefer fewer, larger sprites.
### Fog (Ground)
Very low contrast; distance-scaled; life 2–6 s; disable secondaries at Far LOD.
### Dust Storm Sheets
Wide sprites with low-freq panners; random per-emitter UV offset; clamp bright albedo to avoid banding.
## QA Checklist
No frame pops; intersections stay soft; opacity never hard-cuts; perf stable at 60/120 fps.
## Release Notes
v2 — merged from smoke-steam setup, depthfade+subuv, and subuv renderer notes.
## Version notes
- Tested 5.1/5.3/5.4.
- If refraction shimmers (5.1–5.2): disable refraction or gate via quality preset.
- If ribbon UVs swim (5.1–5.2): use DistanceAlongRibbon UVs and clamp stretch.
