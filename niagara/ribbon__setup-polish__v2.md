# /niagara/ribbon__setup-polish__v2.md
---
title: "Ribbon — Setup & Polish (Unified)"
id: ribbon_setup-polish_v2
type: lesson
tags: ["lesson","niagara","ribbon","trail","uv","unified","remix:original"]
---
## Overview
Set up reliable ribbon trails with distance-based UVs, width/opacity curves, and anti-twist polish—includes **secondary impact streaks** for projectiles.
## Learning Goals
- Distance/age UV strategies; width from curve; stretch clamps.
- Stable orientation to avoid twist at high curvature.
- Impact-triggered secondary streaks with rapid decay.
## Prerequisites
Ribbon renderer basics; projectile or moving actor.
## Steps (outline)
Ribbon renderer config → material with soft edge & UV from distance → width/opacity curves → stretch clamp by speed → anti-twist orientation hints → **Secondary Streaks**: inherit velocity on impact, lifetime < 0.35s.
## Optional: Sparkle Streaks (Ice)
- Add a low-rate ribbon with **DistanceAlongRibbon UVs**; width 0.2–0.6 cm.
- Material uses crystalline mask in emissive for momentary glints; lifetime 0.08–0.18 s.
- Gate by significance; disable beyond 25–30 m.
## Ribbon Material: Electric Trail
- **UVs:** DistanceAlongRibbon for stable scrolling; optional second UV for spark blips.
- **Look:** narrow core + soft fringe; emissive panner ≤0.6; occasional mask spikes for crackle.
- **Polish:** clamp stretch by speed; lifetime ≤0.25 s; disable trail when beam inactive.
## Add-on Pack — Ember Trails, Electric Trails, Sparkle Streaks
DistanceAlongRibbon UVs; narrow core + soft fringe; lifetime 0.08–0.25 s; clamp stretch by speed; disable beyond 25–30 m; occasional intensity spikes for embers; crystalline mask for ice glints.

## QA Checklist
No twisting or UV swimming; trails cull cleanly; impact streaks don’t spike overdraw.
## Release Notes
v2 — merged from ribbon setup + ribbon polish; adds projectile secondary recipe.
## Version notes
- Tested 5.1/5.3/5.4.
- If refraction shimmers (5.1–5.2): disable refraction or gate via quality preset.
- If ribbon UVs swim (5.1–5.2): use DistanceAlongRibbon UVs and clamp stretch.
