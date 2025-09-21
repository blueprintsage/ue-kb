# Viewport Cost Debugging
**Domain:** materials • **Level:** beginner→int • **Engine:** UE5
## Why
Find why an effect is expensive (shader, overdraw, overdrawn translucency).
## Steps
- Viewport → **Optimization Viewmodes**: Shader Complexity, Quad Overdraw, Light Complexity.
- Material Editor → **Stats**: instruction count, texture samplers; prefer **Material Instances**.
- Cut cost: reduce texture taps, pack masks, avoid nested noise; minimize full-screen SceneDepth sampling.
## Quick Targets
- Translucent quads: keep small, depth-fade, avoid stacking.
- If it glows: clamp emissive; test tone-mapper.
