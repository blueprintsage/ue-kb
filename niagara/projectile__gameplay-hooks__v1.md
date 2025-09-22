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
## QA Checklist
No double-spawns; cleanup on destroy; PIE and packaged parity.
## Release Notes
v1.0 — hooks implemented.
