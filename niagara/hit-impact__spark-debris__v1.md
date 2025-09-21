# Hit Impact — Sparks & Debris
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5

## Recipe
- System with 2 emitters:
  - **Sparks (Ribbon)**: CPU, burst 20–60, high initial velocity, **Ribbon Renderer** (tangent from velocity), width tapers.
  - **Debris (Mesh)**: CPU, burst 5–12, arc under gravity, random mesh scale/rotation.
- Collision: enable with restitution for sparks (small bounce), kill on 2nd hit.
- Color/Alpha over life; sparks short (0.3–0.6s), debris longer (0.8–1.6s).

## Checks
- Clear starburst, quick decay; a few debris pieces arc and land convincingly.

## Pitfalls
- Too few particles → anemic pop; too many → visual noise. Tune bursts per use-case.
