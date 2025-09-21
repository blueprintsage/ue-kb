# GPU Sim — Gotchas
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5

## Quick Rules
- No CPU collision events; use GPU collisions or proxy CPU emitters for events.
- Avoid random heavy **SceneDepth**/texture sampling per-particle; batch via RTs if possible.
- Material complexity matters: prefer unlit, few texture taps, no expensive branches.

## Checks
- Large counts remain stable; profiler shows GPU time in budget.

## Pitfalls
- Trying to read CPU-only data; overdraw storms from huge translucent quads.
