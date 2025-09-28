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
## Add-On: Glowing Particles (Ice)
- Emit tiny additive sprites at impact with **emissive pulse curve** (0 → 1 → 0 in ≤0.12 s).
- Scale light intensity by distance; cooldown to prevent strobing.
## Add-on: Muzzle & Impact Lights
- **Muzzle:** 1–2 frame point-light pulse; radius from weapon tier; cooldown to avoid strobing.
- **Impact:** brief light flash (≤0.08 s) for hot impacts only; skip for electric on Low preset.
- **Camera:** optional light-linked exposure clamp for Sequencer clarity shots.
## Add-on Pack — Muzzle Flash, Glow Particles

### Rifle Muzzle Flash
Additive sprite fan; lifetime 1–2 frames; point light pulse with inverse-distance falloff; cooldown guard; disable on photo-sensitive preset.
### Glowing Particles (Ice/Fire)
Emissive pulse curve (0→1→0 ≤0.12 s); clamp intensity by distance; random seed per shot.
## Add-on Pack — Muzzle & Impact Lights
### Muzzle
1–2 frame point-light pulse; radius by weapon tier; cooldown to avoid strobing.
### Impact
Brief light flash (≤0.08 s) for hot impacts only; skip for electric on Low.
### Camera
Optional exposure clamp track for clarity shots in Sequencer.

## QA Checklist
Comfort-safe; no strobe; works at 60/120 fps.
## Release Notes
v1.0 — light/shake hooks integrated.
