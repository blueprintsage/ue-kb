---
title: G2/k4 — WFC Backtracking & Masks
kit_id: g2_graphs_grammars
version: 1.0
status: Draft
type: kata
---
## Objective
Add backtracking and support for fixed/forbidden masks.
## Tasks
- Maintain a decision stack; on contradiction, backtrack to last choice and try next candidate.  
- Respect fixed tiles and forbidden zones during collapse.
## Acceptance
- [ ] Solves masked problems that simple WFC could not.  
- [ ] Backtrack depth bounded; logs show retries.