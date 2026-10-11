---
name: fplai-run-analysis
description: Run a fresh FPLai analysis for the user's linked FPL team. Use only when the user explicitly asks for a new analysis; it uses their analysis quota.
---
# Run a fresh FPLai analysis

A fresh run consumes the user's analysis quota, so ask first and proceed only after an explicit yes.

1. Call `get_latest_fplai_analysis` first and show what already exists. If it is recent, suggest using it.
2. After the user approves, call `run_fplai_analysis` with a new UUID as `analysisRequestId` and a `horizon` from 1 to 6 (default 1).
3. If the outcome is unclear, check `get_latest_fplai_analysis` before retrying. Reuse the same `analysisRequestId` only for an authorised retry, and warn that retries are not fully idempotent.
4. Summarise the result as in `fplai-squad-review`.
