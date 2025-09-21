# Sequencer Hooks — Tracks & Control
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5

## Goal
Drive Niagara during cinematics.

## Recipe
- Add **Niagara System Track** in Sequencer; key **Activate**, **Deactivate**, and **Parameters** (User floats/vecs).
- For looping systems, cut sections to precise timing; for bursts, key a short activation with zero pre/post-roll.
- Use **Level Sequence** in BP to trigger complex FX choreographies.

## Checks
- FX activate exactly on cues; parameter keys modulate intensity convincingly.

## Pitfalls
- Autokey off → missed keys; forgetting to bind the specific component instance.
