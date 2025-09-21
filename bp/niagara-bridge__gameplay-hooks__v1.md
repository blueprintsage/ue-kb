# BP ↔ Niagara — Gameplay Hooks
**Domain:** bp • **Level:** beginner→int • **Engine:** UE5

## Triggers
- **OnHit/OnOverlap** (Actor or Component) → **Spawn System at Location** (impact FX).
- **Ability pressed** → set `User.Intensity` via **Timeline** (0↔1) for flamethrower/portal growth.
- **Damage events** → map damage → `User.BurstCount` or `User.SparkEnergy`.

## Patterns
- Prefer **Set Niagara Variable (Float/Vec/Bool)** with `User.*` names; avoid Tick—use Timers/Events.
- Cache Niagara Component refs in BeginPlay; don’t repeatedly `GetComponentByClass` in loop.

## Checks
- Toggling inputs clearly scales FX; impacts spawn exactly at hit location/normal.

## Pitfalls
- Variable name mismatches; forgetting to enable input on actors that need it.
