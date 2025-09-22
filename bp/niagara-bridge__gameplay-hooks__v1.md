# BP ↔ Niagara — Gameplay Hooks
**Domain:** bp • **Level:** beginner→int • **Engine:** UE5

## Triggers
- **OnHit/OnOverlap** (Actor or Component) → **Spawn System at Location** (impact FX).
- **Ability pressed** → set `User.Intensity` via **Timeline** (0↔1) for flamethrower/portal growth.
- **Damage events** → map damage → `User.BurstCount` or `User.SparkEnergy`.

## Hook: Player Beam Routing
- **Source:** attach Niagara beam component to player mesh socket (`hand_r` or `weapon_muzzle`).
- **Target:** each tick, line trace from camera or muzzle; set Niagara User Params: `TargetPosition`, `BeamActive`.
- **Events:** on block hit, send `FX.Electric.Hit` (position, normal) → impact systems (sparks/decal) via Spawn Router.
- **Safety:** add cooldown to avoid event spam; reset on component deactivate.

## Patterns
- Prefer **Set Niagara Variable (Float/Vec/Bool)** with `User.*` names; avoid Tick—use Timers/Events.
- Cache Niagara Component refs in BeginPlay; don’t repeatedly `GetComponentByClass` in loop.

## Add-on Pack — Router Patterns
### Bullet Trace → Impact
LineTrace, send `FX.Bullet.Hit` (Loc, Normal, PhysMat); rate limiter for auto fire.
### Molotov
Projectile actor; on impact send `FX.Fire.Puddle.Start`; schedule Stop; clean decals/lights.
### Player Beam
Attach beam comp to socket; tick trace to set Target; on block → `FX.Electric.Hit`; reset on deactivate.
### AOE Beats (Anticipation → Climax → Settle)
Expose User Params: Scale, Color, Intensity; Timeline: Anticipation curve → Climax spike → Settle tail; single source of truth for all emitters.


## Checks
- Toggling inputs clearly scales FX; impacts spawn exactly at hit location/normal.

## Pitfalls
- Variable name mismatches; forgetting to enable input on actors that need it.
