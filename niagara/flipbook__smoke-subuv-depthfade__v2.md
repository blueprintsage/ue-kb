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
## QA Checklist
No frame pops; intersections stay soft; opacity never hard-cuts; perf stable at 60/120 fps.
## Release Notes
v2 — merged from smoke-steam setup, depthfade+subuv, and subuv renderer notes.
## Version notes
- Tested 5.1/5.3/5.4.
- If refraction shimmers (5.1–5.2): disable refraction or gate via quality preset.
- If ribbon UVs swim (5.1–5.2): use DistanceAlongRibbon UVs and clamp stretch.
