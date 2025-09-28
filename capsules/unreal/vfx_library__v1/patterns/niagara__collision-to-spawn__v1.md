# PAT: Collision → Spawn (Splashes/Impacts)
**Purpose:** Spawn secondary FX (splash, debris) when particles hit.
**Chain:** Emitter A (drops): Collision + **Generate Collision Event** → System Emitter B listens via **Event Handler (Collision)** → **Spawn Burst Instantaneous** using Event Position/Normal.
**Params:** Velocity threshold; normal dot (e.g., Up·Normal > 0.6) to keep ground-only.
**Checks:** Visible splash exactly at impact; wall hits filtered if desired.
**Pitfalls:** GPU sprites may not emit CPU events; bind handler to the right source emitter.
