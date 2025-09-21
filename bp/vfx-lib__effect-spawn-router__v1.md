# BP VFX Library — Effect Spawn Router
**Domain:** bp • **Level:** beginner→int • **Engine:** UE5
## Goal
Route gameplay events (hit, ability, status) → named FX with parameters.
## Implementation
- Create `BP_VFXRouter` with `DataTable<RowName, NiagaraSystem>` + struct of defaults.
- Functions: `SpawnAtLocation(FXName, Loc, Norm, Overrides)`; `SetGlobal(MPCName, Param, Value)`.
- Usage: Actors call router on hit/ability; router looks up system & spawns; apply overrides to `User.*`.
## Checks
- One-line calls from gameplay; easy swap of FX via DataTable.
