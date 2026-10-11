# FPLai plugin for Grok, Cursor and other MCP clients

Connect your [FPLai](https://fplai.app) account so Grok can read your Fantasy Premier League analysis, compare players and (with your approval) run a fresh analysis.

## What it adds
- Remote MCP server `https://mcp.fplai.app/mcp` (Streamable HTTP, OAuth sign-in with your FPLai account).
- Skills: `fplai-squad-review`, `fplai-compare-players`, `fplai-run-analysis`.

## MCP tools
`get_fplai_account`, `get_latest_fplai_analysis`, `get_fplai_analysis`, `compare_fplai_players`, `run_fplai_analysis`.

## Network and credentials
- Calls only `https://mcp.fplai.app`.
- Sign-in is OAuth in your browser; no API keys or passwords are stored in this plugin.
- No hooks, no scripts, no local code execution.
- Full results need an FPLai Pro or Season Pass plan; free accounts get limited results.
- `run_fplai_analysis` uses your analysis quota and only runs after you approve it.

## Support and privacy
https://fplai.app

## Licence
MIT

## Install
- **Grok Build:** install `fplai` from the xAI plugin marketplace.
- **Cursor:** install `fplai` from the Cursor Marketplace or cursor.directory.
- **Any MCP client:** add the server URL `https://mcp.fplai.app/mcp` as a custom remote MCP server and sign in with your FPLai account.
