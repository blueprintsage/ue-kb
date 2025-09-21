# Flamethrower — Main Flame
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5

## Recipe
- System `NS_Flamethrower`, Emitter `EM_Flame` (GPU Sprite for count).
- Shape Location: **Cone** (narrow angle). **Spawn Rate** high + short **Lifetime** (0.25–0.6s).
- Init Velocity: strong forward with small spread; **Scale Sprite Size by Velocity** for stretch.
- Material: fiery flipbook (SubUV Life, 1 loop). **Color Over Life**: core hot → tail dim.
- Optional: user float `User.Intensity` multiplies Spawn Rate for BP control.

## Checks
- Press/hold intensity → continuous jet; release → instant stop; frames read as fast flame.
## Pitfalls
- Too much drag kills stretch; too little causes noisy jitter—tune with small Curl + modest Drag.
