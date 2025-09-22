# /bp/projectile__gameplay-hooks__v1.md
---
title: "Projectile — Gameplay Hooks"
id: projectile_gameplay-hooks_v1
type: lesson
tags: ["lesson","bp","events","cleanup","remix:original"]
---
## Overview
Wire notifies/overlaps/timers to drive muzzle, trail, impact, and cleanup in sync with gameplay.
## Learning Goals
- Deterministic order of events.
- Clear destroy/cleanup path.
## Prerequisites
BP anim notifies, overlaps, timers.
## Steps (outline)
Notify → spawn muzzle/trail; overlap → impact; timer → cleanup; router in the middle.
## Add-on: Projectile Router & Scale/Color Controls
- **Router tags:** `FX.Projectile.Muzzle`, `FX.Projectile.Trail`, `FX.Projectile.Impact`.
- **Easy controls:** MPC keys `FX_Scale` (sizes/speeds/bounds) and `FX_Tint`; single DT row applies both.
- **Capsule setup (electric variant):** spawn from socket, set `Target` each tick; send `FX.Electric.Hit` on block.
## Add-on Pack — Router Patterns
### Bullet Trace → Impact
LineTrace, send `FX.Bullet.Hit` (Loc, Normal, PhysMat); rate limiter for auto fire.
### Molotov
Projectile actor; on impact send `FX.Fire.Puddle.Start`; schedule Stop; clean decals/lights.
### Player Beam
Attach beam comp to socket; tick trace to set Target; on block → `FX.Electric.Hit`; reset on deactivate.
### Projectile Router & Scale/Color Controls
Tags: `FX.Projectile.Muzzle`, `FX.Projectile.Trail`, `FX.Projectile.Impact`. MPC keys `FX_Scale` (sizes/speeds/bounds) + `FX_Tint`; DataTable row applies both.
### AOE Beats (Anticipation → Climax → Settle)
Expose User Params: Scale, Color, Intensity; Timeline: Anticipation curve → Climax spike → Settle tail.
## QA Checklist
No double-spawns; cleanup on destroy; PIE and packaged parity.
## Release Notes
v1.0 — hooks implemented.
