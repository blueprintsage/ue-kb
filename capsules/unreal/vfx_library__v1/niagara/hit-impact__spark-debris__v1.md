# Hit Impact — Sparks & Debris
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5

## Recipe
- System with 2 emitters:
  - **Sparks (Ribbon)**: CPU, burst 20–60, high initial velocity, **Ribbon Renderer** (tangent from velocity), width tapers.
  - **Debris (Mesh)**: CPU, burst 5–12, arc under gravity, random mesh scale/rotation.
- Collision: enable with restitution for sparks (small bounce), kill on 2nd hit.
- Color/Alpha over life; sparks short (0.3–0.6s), debris longer (0.8–1.6s).

## Variant: Icy Shards
- Replace sparks with **mesh shards (icicle LOD0/1)**; inherit impact normal for initial velocity.
- Add tiny **glints**: additive sprites with short (≤0.12 s) emissive pulse using the ice rim mask.
- Limit shard count (6–12); smoke puff optional (see Cold Smoke preset).

## Variant: Electric Ground Sparks
- **Spawn:** on `FX.Electric.Hit`; short-lived additive sprites (≤0.12 s) with bright pulse → decay.
- **Direction:** bias velocity along surface tangent; a few upward pops for variety.
- **Extras:** tiny decal scorch (DBuffer) with 0.6–1.0 s fade; optional sound cue.
- **Perf:** very low count; gate scorch decals on Low preset.

## Add-on Pack — Sparks, Bullets, Electric, Explosion, Water/Blood

### Sparks (Core)
2–8 additive sprites ≤0.12 s; tangent-biased vel; optional ribbon streaks.
### Bullet Impact FX
Micro puff (dust/metal), 1–3 chips on hard surfaces; order: decal → puff → sparks (frame-staggered).
### Electric Ground Sparks
Spawn on `FX.Electric.Hit`; bright pulse ≤0.12 s; scorch decal optional, gated on Low.
### Explosion Burst (Hot)
1-frame fire burst; 12–40 hot sparks; 2–6 debris; smoke delayed 0.05–0.1 s.
### Water/Blood Splash Particles
Short droplets arc; use collision kill on second bounce; darker tint ↘ alpha quickly to avoid clutter.


## Checks
- Clear starburst, quick decay; a few debris pieces arc and land convincingly.

## Pitfalls
- Too few particles → anemic pop; too many → visual noise. Tune bursts per use-case.
