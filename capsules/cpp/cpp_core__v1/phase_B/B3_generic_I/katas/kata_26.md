---
title: B3/k26 — CPO Pattern (Customization Point Objects)
kit_id: b3_generic_I
version: 1.0
status: Draft
type: kata
---
## Objective
Expose an algorithm via inline `constexpr` object calling ADL‑found `tag_invoke` or free function.
## Acceptance
- [ ] Works with user types without extra includes; overload set stays stable.