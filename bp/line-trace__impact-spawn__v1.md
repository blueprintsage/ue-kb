# BP Line Trace → Impact FX Spawn
**Domain:** bp • **Level:** beginner • **Engine:** UE5
## Graph (Actor/Pawn)
- Input (Fire/Click) → **LineTraceByChannel** (Start=Camera, End=Start + Forward*Range).
- **Break Hit** → Location/ImpactNormal.
- **Spawn System at Location** (Hit Impact NS); set **User.Normal** from ImpactNormal; **Spawn Decal at Location** with rot-from-normal.
## Tips
- Add surface switch: PhysicalMaterial → choose FX/decal set; cooldown to avoid spam.
