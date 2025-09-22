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
## QA Checklist
No z-fighting; decal lifespan < 1.2s; smoke opacity never hard-cuts.
## Release Notes
v1.0 — pooled decal/smoke combo.
