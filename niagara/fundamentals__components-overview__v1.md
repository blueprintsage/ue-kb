# Niagara Components Overview
**Domain:** niagara • **Level:** beginner • **Engine:** UE5  
**Objective:** Know System/Emitter/Modules/Renderer and where User params live.
## Add-on Pack — Readability Principles (from UE4 Fundamentals)
Gameplay: primary read first, secondaries support.  
Timing: anticipation→impact→settle; don’t let tails hide gameplay.  
Shape: bold silhouette at Near/Mid; avoid noisy thin lines at Far.  
Contrast: luminance > color; ensure silhouette reads in grayscale.  
Color: hue separation from background; cap emissive; presets per biome.
## Add-on Pack — Readability Principles (UE4→UE5)
### Gameplay
Primary read first; secondaries only support the action.
### Timing
Anticipation → Impact/Climax → Settle; tails mustn’t obscure gameplay.
### Shape
Bold silhouette for Near/Mid; avoid thin noisy detail at Far.
### Contrast
Prioritize luminance contrast; do a quick grayscale check; clamp emissive.
### Color
Separate hue from background/biome; keep preset palettes consistent; avoid clipping.
## Add-on Pack — Stylized VFX Goals (Course Intro)
Audience: beginners→intermediate aiming for readable, stylized reads in UE5.
Pillars: Bold shape, controlled contrast, tight color story, minimal noise, performance-first.
Workflow loop: Reference → Sketch beats → Block in (primitive mats) → Readability pass → Polish → QA.
Deliverables: one projectile style set (core/trail/impact) + capture-ready scene.
Common traps: too many secondaries, thin noisy detail at Far, unbounded emissive, overdraw spikes.
## Notes
- **System** owns one+ **Emitters**. Emitters have **Spawn/Update** stacks with modules (Spawn Rate, Init Velocity, Color Over Life, etc.).  
- **Renderer** (Sprite/Ribbon/Mesh) is configured outside the emitter.  
- **Parameters:** Engine, Emitter, and **User.***User** exposes values to BP and per-instance tuning.

## Checks
- You can locate Spawn vs Update; you can add Drag; you can explain why **User.* ** beats hard-coded numbers.
