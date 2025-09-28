# /niagara/projectile__impact-decal-smoke__v1.md
---
title: "Projectile — Impact Decal + Smoke"
id: projectile_impact-decal-smoke_v1
type: lesson
tags: ["lesson","niagara","impact","decal","smoke","remix:original"]
---
## Overview
Spawn a brief impact decal and a puff of smoke using collision events—cheap, readable, and pooled.
## Learning Goals
- Decal normal-aligned with timed fade.
- Smoke flipbook with depth-fade.
## Prerequisites
Niagara events; decal material basics.
## Steps (outline)
Collision event → spawn DecalSys + SmokeSys → timed cleanup via user params.
## Add-on: Impact Presets (Magic/Electric)
- **Magic:** soft shock-ring + faint scorch; flipbook puff 0.15–0.35 s; lights OFF by default.
- **Electric:** micro scorch decal (DBuffer) + bright spark burst (≤0.12 s) → tiny smoke delay 0.05 s.
- **Order guard:** decal → burst/sparks → smoke; single-frame staggering to reduce overdraw spikes.
## Add-on Pack — Molotov / Splash Impacts
### Fire Splash (Molotov)
Quick scorch decal (size from bottle radius) + warm smoke ring burst; brief point-light pulse ≤0.12 s.
### Water Splash
Tiny wet decal ring; upward splash puff ≤0.25 s; no light; pool aggressively.
## Add-on Pack — Molotov / Splash Impacts
### Fire Splash (Molotov)
Quick scorch decal (size from bottle radius) + warm smoke ring burst; brief point-light pulse ≤0.12 s.
### Water Splash
Tiny wet decal ring; upward splash puff ≤0.25 s; no light; pool aggressively.
### Impact Presets (Electric/Magic)
Electric: micro scorch + bright spark burst (≤0.12 s) → tiny smoke 0.05 s later.
Magic: soft shock-ring + faint scorch; lights OFF by default.
## Add-on Pack — Projectile System Build (Niagara)
System: `NS_Proj_Stylized`; Emitters: `Muzzle_Flash`, `Trail_Ribbon`, `Impact_Burst`, `Impact_Smoke`.
Order of ops (1 frame offsets): Muzzle → Trail start → Impact decal → Burst → Smoke.
Curves: lifetime and spawn tied to `FX_Scale`; determinism ON for router-driven gameplay.
QA hooks: bounds presets per scale; significance gating removes smoke at Far.
## QA Checklist
No z-fighting; decal lifespan < 1.2s; smoke opacity never hard-cuts.
## Release Notes
v1.0 — pooled decal/smoke combo.
