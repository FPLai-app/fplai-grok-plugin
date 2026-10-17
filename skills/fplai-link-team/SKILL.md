---
name: fplai-link-team
description: Link the user's own Fantasy Premier League team to their FPLai account from the chat. Use when no FPL team is linked, when a tool returns TEAM_NOT_LINKED or TEAM_RELINK_REQUIRED, or when the user asks to connect or change their FPL team.
---
# Link an FPL team

1. Ask for the user's FPL team name or FPL team ID (the number after `/entry/` on the FPL Points page), or their official team link.
2. Call `find_fpl_team` with what they gave. Show the candidates (team name, manager as first name and last initial, overall rank) and let the user pick. Never guess a team from a web search or pick one for the user. If name search is unavailable, ask for the team ID.
3. Call `link_fpl_team` with the chosen `entryId` and no `confirm`. This changes nothing and returns a `confirmationId`. Ask "Is <team> your team?".
4. Only after a clear yes, call `link_fpl_team` again with the same `entryId`, `confirm: true` and the `confirmationId`. FPLai then shows its own yes/no prompt, and only that answer links the team; a "no", cancel or timeout changes nothing.
5. If the result is `link_on_website`, nothing was linked: give the user the returned `url`, where they confirm the team on FPLai themselves.
6. An account has one linked team. If the preview returns `already_linked` with another team, ask whether to replace it and only then preview again with `replaceExisting: true`.

Linking never runs an analysis. Offer one afterwards and run it only if the user asks (see `fplai-run-analysis`).
