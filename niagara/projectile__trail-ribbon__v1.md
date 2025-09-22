# /niagara/projectile__trail-ribbon__v1.md
---
title: "Projectile — Trail (Ribbon)"
id: projectile_trail-ribbon_v1
type: lesson
tags: ["lesson","niagara","trail","ribbon","projectile","remix:original"]
---
## Overview
Create a ribbon trail with stable UVs, lifetime-based fade, and velocity stretch without jitter.
## Learning Goals
- Consistent width and clean UV flow.
- Lifetime & speed drive opacity/tilt.
## Prerequisites
Niagara ribbon renderer basics.
## Steps (outline)
Ribbon system → width from curve → UVs from distance → material with soft edge and stretch clamp.
## QA Checklist
No twisting at sharp turns; trail culls cleanly; perf within budget.
## Release Notes
v1.0 — baseline trail with tunable lifetime.
