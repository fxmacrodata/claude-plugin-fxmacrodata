---
description: Research currency history alongside policy, curves, positioning and commodity context
argument-hint: "<base currency> <quote currency> [date range or question]"
---

# Currency context

Use both research skills. Resolve the base and quote explicitly; never reverse a quoted pair without stating the conversion.

1. Use `data_catalogue` to establish coverage and pair availability, then `forex` for the rate history, following the connected tool schema. Reference rates are not executable quotes.
2. Use `rate_differentials`, `rate_curve` and `indicator_query` to add policy and curve context. Check whether observations share an as-of date and unit before deriving a spread. Keep each original series definition and source.
3. If entitled and relevant, use `cot_data`, `commodities`, `risk_sentiment` and `seasonality`. Use `market_sessions` for session context. Unavailable data must not be replaced with another provider or a guessed value.
4. `event_impact_replay_task`, `fx_backtest_task` and `fx_trade_setup_task` can test a requested idea against history. Label assumptions and outputs, and distinguish them from observed data. Do not present a backtest or setup as a forecast or guaranteed return.
5. Return the requested comparison, a source/timing table and explicit access or coverage gaps. Use the matching visual tool only if the host can render it; otherwise provide a readable table.

FX pairs and optional datasets may need subscriber access. Never ask for credentials in the conversation or insert them into tool arguments or URLs.
