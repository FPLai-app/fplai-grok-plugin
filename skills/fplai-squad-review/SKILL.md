---
name: fplai-squad-review
description: Review the user's current Fantasy Premier League squad using their saved FPLai analysis (captain, transfer, chips). Use when they ask about their FPL team, captain, transfers or chips.
---
# FPLai squad review

1. Call `get_fplai_account` to see the tier and whether an FPL team is linked. If no team is linked, tell the user to link their team at https://fplai.app and stop.
2. Call `get_latest_fplai_analysis` and summarise it in plain words: recommended transfer, captain and vice-captain, chip advice, and the confidence level with its stated caveats.
3. Say when the analysis was created and for which gameweek. If it looks stale, offer a fresh run, but never start one without the user's explicit approval (see the `fplai-run-analysis` skill).
4. Be honest about uncertainty: report the calibrated gain and confidence exactly as FPLai gives them. Do not invent players, numbers or fixtures.
