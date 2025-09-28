---
title: A5/k2 — placement new
kit_id: a5_new_delete_variants
version: 1.0
status: Draft
type: kata
---
## Goal
Construct object in pre-allocated buffer; manually call destructor.
## Task
Use `char buf[sizeof(Widget)]; new(buf) Widget(); reinterpret_cast<Widget*>(buf)->~Widget();`
## Acceptance
- [ ] No leaks/UB under ASan.