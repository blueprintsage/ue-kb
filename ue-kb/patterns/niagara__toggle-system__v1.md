# PAT: Toggle Niagara System (On/Off)
**Purpose:** Simple enable/disable, with optional smooth fade.
**BP:** Input/Trigger → **FlipFlop** → **Set Niagara System Active (false/true)**.
**Optional fade:** **Timeline(0↔1, 0.5–0.8s)** → **Set Niagara Variable (Float)** name "User.SpawnRateMult".
**Checks:** Press once → fades/stops; press again → fades/plays.
**Pitfalls:** Target not set to the Niagara component; missing User param in Niagara graph.
