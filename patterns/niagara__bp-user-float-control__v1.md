# PAT: BP ↔ Niagara — User Float Control
**Purpose:** Drive effect intensity from Blueprints without Tick.
**Niagara:** Create `User.Float SpawnRateMult` and multiply it into your Spawn Rate (or any curve).
**Blueprint:** `Timeline(Float 0↔1, 0.5–1.0s)` → `Set Niagara Variable (Float)` name `"User.SpawnRateMult"`.
**Checks:** Scrubbing the timeline thins/thickens live; 0 silences spawns (if multiplied).
**Pitfalls:** Name mismatch; not exposing the User param in the graph; using Tick instead of a Timeline/Timer.
