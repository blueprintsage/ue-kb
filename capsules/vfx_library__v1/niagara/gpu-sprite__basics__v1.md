# GPU Sprite — Basics
**Objective:** Use GPU sprites for heavy counts.
## Recipe
- Emitter: change **Sim Target** to **GPUCompute Sim**.
- Keep modules supported on GPU; for collision events, use CPU or alternative logic.
## Checks
- Large Spawn Rate stays smooth; note event limitations vs CPU sprites.
