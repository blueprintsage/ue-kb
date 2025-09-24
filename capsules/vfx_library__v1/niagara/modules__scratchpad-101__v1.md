# Custom Module — Scratchpad 101
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5

## Goal
Author a quick per-particle math tweak without leaving the system.

## Recipe
- In an emitter stack: **Add Module → New Scratch Pad Module**.
- Add **Inputs**: e.g., `User.Float Scale = 1.0`; **Outputs**: e.g., `Velocity`, `Color`.
- Graph: `Velocity *= Scale;` (or Add, Clamp, etc.). Expose inputs as **User.*** for BP.
- Save as **Local (in system)** for fast iteration.

## Checks
- Tuning `Scale` changes motion live; module order affects results predictably.

## Pitfalls
- Forgetting to set defaults; writing to attributes not present in this stage.
