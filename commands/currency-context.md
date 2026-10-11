---
description: Research currency history alongside policy, curves, positioning and commodity context
argument-hint: "<base currency> <quote currency> [date range or question]"
---

# Currency context

Use both research skills. Resolve the base and quote explicitly; never reverse a quoted pair without stating the conversion.

1. Use `fx_reference_sources` and `fx_reference_universe` where available to establish source coverage, frequency and pair availability. Select `forex` or `fx_intraday_reference_rates` according to the user's question and the connected tool schema. Reference rates are not executable quotes.
2. Use `rate_differentials`, `rate_curve` and `indicator_query` to add policy and curve context. Check whether observations share an as-of date and unit before deriving a spread. Keep each original series definition and source.
3. If entitled and relevant, use `cot_data`, `commodities`, `latest_commodities`, `risk_sentiment`, `macro_factor` and `financial_prices`. Use `risk_sentiment_changes` for retained sentiment changes when requested, following `pagination.next_after_sequence` with `after_sequence`; do not treat a partial page as a complete change history. Use `market_sessions` for session context. Unavailable data must not be replaced with another provider or a guessed value.
4. `pair_intel_task`, `policy_scenario_modeler_task` and `quant_scenario_lab_task` can help structure a requested scenario. Label assumptions and outputs, and distinguish them from observed data. Do not present a scenario as a forecast or guaranteed return.
5. Return the requested comparison, a source/timing table and explicit access or coverage gaps. Use the matching visual tool only if the host can render it; otherwise provide a readable table.

FX pairs and optional datasets may need subscriber access. Never ask for credentials in the conversation or insert them into tool arguments or URLs.
