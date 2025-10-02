---
title: G2/k1 — L‑System Basics (Deterministic)
kit_id: g2_graphs_grammars
version: 1.0
status: Draft
type: kata
---
## Objective
Implement a string‑rewriting L‑system and a simple turtle interpreter.
## Tasks
- Parse axiom and rules like `A->AB`, `B->A`; iterate N times.  
- Turtle: `F` forward, `+/-` rotate, `[/]` push/pop transform.
## Acceptance
- [ ] Known derivations match examples; drawing stable.  
- [ ] No stack under/overflow in deep branches.