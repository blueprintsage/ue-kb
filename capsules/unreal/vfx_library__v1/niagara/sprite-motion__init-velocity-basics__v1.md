# Sprite Motion: Init Velocity Basics
**Domain:** niagara • **Level:** beginner • **Engine:** UE5

## Recipe
- Init Velocity: X/Y jitter ±15, Z = 60.  
- Gravity: off for smoke; on (-980) for debris.  
- Size: 32–48 with a little random.  
- Alpha fades out over last 25% of life.

## Checks
- Gravity toggle clearly changes arc; motion is stable (no random acceleration thrash).
