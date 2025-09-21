# Blueprint Variables — Carry Card
**Domain:** bp • **Level:** beginner • **Engine:** UE5

## Types at a glance
Bool (toggle), Int (count), Float (tunable), Name (IDs), Text (UI), Vector/Rotator/Transform (space), Enum/Struct (state/bundles), Array/Map/Set (collections).

## Golden settings
Instance Editable • Expose on Spawn • Category grouping • sensible Defaults.

## Comm patterns
Direct ref (tight) • Interfaces (clean) • Dispatchers (broadcast) • Subsystems (global). Avoid Tick spam—prefer Timers/Events.
