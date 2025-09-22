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
## Add-on: Trail Variants (Electric, Magic)
- **UVs:** DistanceAlongRibbon; second UV channel for crackle blips.
- **Width:** near = thicker core; mid/far = taper + opacity drop; clamp stretch by speed.
- **Electric:** short lifetime 0.08–0.18 s with intensity spikes; disable beyond 25–30 m (significance).
- **Magic:** “steppy” motion option: quantize panner (0.0/0.02/0.04…) for stylized look.

## QA Checklist
No twisting at sharp turns; trail culls cleanly; perf within budget.
## Release Notes
v1.0 — baseline trail with tunable lifetime.
