---
name: fplai-compare-players
description: Compare two or more FPL players using FPLai projections. Use when the user asks who to pick between players.
---
# FPLai player comparison

1. Call `compare_fplai_players` with up to 5 players. Prefer numeric `playerIds`; use exact web names in `playerNames` only when they are unambiguous. Names are matched exactly, never fuzzily. Optionally set `horizon` (1 to 6 gameweeks).
2. Present the projections side by side and give a short recommendation. Free accounts may get a teaser result; say so rather than guessing the missing detail.
3. Do not fill gaps with numbers from memory.
