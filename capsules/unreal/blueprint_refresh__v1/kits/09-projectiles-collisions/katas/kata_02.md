---
title: BR09/k2 — Damage debug & variable route
kit_id: br09_projectiles
version: 1.0
status: Draft
type: kata
---
## Goal
Expose damage and confirm impact data path.
## Task
Projectile variable Damage (float); on hit, print Damage+HitActor name; broadcast event with (Loc, Normal, Actor, Damage).
## Acceptance
- [ ] Logs show correct values; listener receives event exactly once.