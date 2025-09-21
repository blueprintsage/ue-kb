# Niagara Components Overview
**Domain:** niagara • **Level:** beginner • **Engine:** UE5  
**Objective:** Know System/Emitter/Modules/Renderer and where User params live.

## Notes
- **System** owns one+ **Emitters**. Emitters have **Spawn/Update** stacks with modules (Spawn Rate, Init Velocity, Color Over Life, etc.).  
- **Renderer** (Sprite/Ribbon/Mesh) is configured outside the emitter.  
- **Parameters:** Engine, Emitter, and **User.***User** exposes values to BP and per-instance tuning.

## Checks
- You can locate Spawn vs Update; you can add Drag; you can explain why **User.* ** beats hard-coded numbers.
