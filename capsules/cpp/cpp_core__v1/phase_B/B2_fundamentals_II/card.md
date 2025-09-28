---
title: B2 — Fundamentals II (strings, fmt, i/o, chrono)
kit_id: b2_fundamentals_II
version: 1.0
status: Draft
category: C++ Core
assets: []
dependencies: []
---


## Objective
Master modern text handling, formatting, files/streams, time, and small utilities so everyday C++ feels clean and sharp.


## Steps
1) **Strings:** `std::string`, `std::string_view`, encoding basics, safe slicing.
2) **Formatting:** `std::format` / `fmtlib`, compile‑time format checks.
3) **I/O:** file streams vs `std::filesystem`; binary vs text; buffering.
4) **Time:** `std::chrono` clocks, durations, time zones, formatting/parsing.
5) **Parsing:** `from_chars`/`to_chars` for numbers; error handling.
6) **Small utils:** `span`, `expected`, `scoped_lock`, RAII file guards.


## Smoke Test
- [ ] No dangling views; I/O robust to missing files; time zone ops correct; format strings validated.


## Notes
Prefer value types + views (`string_view`, `span`) for read‑only; lean on `std::format`/`chrono` for clarity and locale safety.