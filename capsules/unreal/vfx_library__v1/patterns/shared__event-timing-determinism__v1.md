# /patterns/shared__event-timing-determinism__v1.md
---
title: "Pattern — Event Timing Determinism"
id: pattern_event-timing-determinism_v1
type: pattern
tags: ["pattern","events","determinism","remix:original"]
---
## Intent
Guarantee muzzle → trail → impact → cleanup order at 60/120 fps.
## Steps (outline)
Single router entrypoint → queue events with timestamps → process in fixed order → cooldown guards.
## Acceptance
Order never inverts in 1k-run test; jitter <1 frame; logs once on missed events.
