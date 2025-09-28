---
title: BR11/k1 — Range-gated attack with cooldown
kit_id: br11_bb_attack_investigate
version: 1.0
status: Draft
type: kata
---
## Goal
Attack only in range, respect cooldown.
## Given
Blackboard `TargetActor`.
## Task
Task_Attack: if Distance<=Range & `bCanAttack` → play montage then set `bCanAttack=false` and start a timer to reset.
## Acceptance
- [ ] No attacks out of range.
- [ ] Back-to-back attacks respect cooldown.