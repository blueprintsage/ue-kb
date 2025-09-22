# VFX Playground Setup
**Domain:** niagara • **Level:** beginner • **Engine:** UE5

## Recipe
- Project: Games → Blank → Blueprint; enable **Niagara** (restart).
- Level: `VFX_Playground` (neutral lighting), camera bookmark for consistent framing.
- Folders: `/VFX/{Systems,Emitters,Materials,Textures/Flipbooks,Meshes,Curves}`.
- Starter system: Template **Fountain** → `NS_SmokeTest` (Sprite renderer, flipbook-ready).
## Add-on Pack — Template & Wind
Third Person template okay; keep tests in `/VFX/*/`.  
Wind MPC keys (`Wind_Speed`, `Wind_Dir`) sampled in smoke/fog materials; beginner maps for Smoke_Steam/Fire/Env.
## Add-on Pack — Template & Wind
Use the Third Person template; keep test content under `/VFX/<topic>/` maps.
Create beginner maps: `Smoke_Steam`, `Fire`, `Env_Weather`, `Projectiles_Sandbox`.
Add an MPC for wind: `Wind_Speed`, `Wind_Dir` (unit vector); sample in smoke/fog/dust materials.
Include a Sequencer test level with a preroll track (2–4 s) to validate loops before capture.
## Add-on Pack — UE5 Scene Setup (Stylized)
Project settings: mobile HDR ON if targeting, AA = TSR/FXAA by platform; bloom clamp conservative.
Maps: `Stylized_Sandbox`, `Stylized_Biome_Desert`, `Stylized_Biome_Snow`; shared Sky/Exp assets.
PostProcess: disable auto-exposure for capture maps; add color grading via LUT per biome.
Preview rigs: target dummies + collision plates (metal/stone/dirt) for quick material reads.
## Checks
- New system renders sprites; changing Spawn Rate clearly changes density.
- SubUV-ready settings available on the Sprite renderer.
