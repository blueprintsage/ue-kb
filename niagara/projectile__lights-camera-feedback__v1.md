# /niagara/projectile__lights-camera-feedback__v1.md
---
title: "Projectile — Lights & Camera Feedback"
id: projectile_lights-camera-feedback_v1
type: lesson
tags: ["lesson","niagara","lights","camera-shake","feedback","remix:original"]
---
## Overview
Add tiny point light pulses and a gentle camera impulse on fire/impact for feel without fatigue.
## Learning Goals
- Intensity scaled by distance; safe shake.
- Optional on low preset.
## Prerequisites
Basic BP/Niagara interaction.
## Steps (outline)
Emit gameplay events → BP adds light pulse + minimal shake → clamp & cooldown; user toggles per quality.
## QA Checklist
Comfort-safe; no strobe; works at 60/120 fps.
## Release Notes
v1.0 — light/shake hooks integrated.
