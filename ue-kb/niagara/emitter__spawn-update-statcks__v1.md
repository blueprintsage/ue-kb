# Emitter Stages: Spawn & Update
**Domain:** niagara • **Level:** beginner • **Engine:** UE5

## Recipe
- In **Update**, order matters: **Forces** → **Drag** → **SolveForcesAndVelocity** → **Integrate** → Color/Size.  
- Add **Curl Noise Force** (10–20), then **Drag** (0.2–0.4).

## Checks
- Motion meanders gently; changing Drag predictably dampens drift.
