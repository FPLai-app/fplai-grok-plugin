---
name: fplai-compare-players
description: Compare two or more FPL players using FPLai projections. Use when the user asks who to pick between players.
---
# FPLai player comparison

1. Call `compare_fplai_players` with up to 5 players. Use numeric `playerIds` when known, otherwise `playerNames` as the user typed them: matching ignores case and accents and accepts surname, full name or initial forms ("Gross", "M.Salah"). Optionally set `horizon` (1 to 6 gameweeks).
2. If the result has `status: needs_clarification`, show the returned `candidates` (ambiguous name) or `suggestions` (name not in this season's FPL player list) and ask the user to choose; never guess.
3. Present the projections side by side and give a short recommendation. Free accounts may get a teaser result; say so rather than guessing the missing detail.
4. Do not fill gaps with numbers from memory.
