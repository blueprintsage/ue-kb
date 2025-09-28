---
title: B1/k22 — `string_view` Lifetimes
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Use `string_view` without dangling.
## Tasks
- Add tests where view outlives source; catch with sanitizer; refactor API to accept owning `std::string` where needed.
## Acceptance
- [ ] No dangling views; documented lifetime rules.