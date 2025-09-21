# VFX Playground Setup
**Domain:** niagara • **Level:** beginner • **Engine:** UE5

## Recipe
- Project: Games → Blank → Blueprint; enable **Niagara** (restart).
- Level: `VFX_Playground` (neutral lighting), camera bookmark for consistent framing.
- Folders: `/VFX/{Systems,Emitters,Materials,Textures/Flipbooks,Meshes,Curves}`.
- Starter system: Template **Fountain** → `NS_SmokeTest` (Sprite renderer, flipbook-ready).

## Checks
- New system renders sprites; changing Spawn Rate clearly changes density.
- SubUV-ready settings available on the Sprite renderer.
