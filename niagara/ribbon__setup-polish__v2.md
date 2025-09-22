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
## QA Checklist
No twisting or UV swimming; trails cull cleanly; impact streaks don’t spike overdraw.
## Release Notes
v2 — merged from ribbon setup + ribbon polish; adds projectile secondary recipe.
## Version notes
- Tested 5.1/5.3/5.4.
- If refraction shimmers (5.1–5.2): disable refraction or gate via quality preset.
- If ribbon UVs swim (5.1–5.2): use DistanceAlongRibbon UVs and clamp stretch.
