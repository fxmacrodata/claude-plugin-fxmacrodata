# FXMacroData connector

The native host connects over HTTP to `https://mcp.fxmacrodata.com/mcp`. The default configuration is keyless. Tools are discovered dynamically; their connected input schemas are authoritative. This reference documents the plugin's workflow coverage without freezing the server's tool list.

All listed tools are available through the host's ordinary MCP tool selection. The macro-research command routes requests across them; the focused commands combine relevant tools into usable work products. Access and App rendering support vary by tool and host.

| Tools | Use | Native workflow |
|---|---|---|
| `ping`, `mcp_capabilities` | Connection health and capability guidance | connection-check |
| `data_catalogue`, `catalogue_search`, `catalogue_related` | Find currencies, indicators, definitions and related series | macro-brief / macro-research |
| `indicator_query`, `latest_announcements` | Indicator histories, latest releases, actual publication evidence and revisions | macro-brief / release-context |
| `release_calendar`, `event_predictions` | Confirmed release schedules and release predictions | release-context |
| `macro_news`, `press_releases` | Official publisher news and statements | macro-brief / macro-research |
| `forex`, `rate_curve`, `rate_differentials` | FX rates, yield curves and policy-rate differentials | currency-context / pair-brief |
| `cot_data`, `commodities`, `risk_sentiment`, `market_sessions`, `seasonality` | Positioning, commodities, sentiment, sessions and seasonal patterns | currency-context / macro-research |
| `official_datasets` | Official dataset families and their components | macro-research |
| `organisation_search`, `organisation_profile` | Official organisations and their publications | macro-research |
| `geopolitical_history`, `geopolitical_event`, `geopolitical_event_reaction`, `geopolitical_event_revisions`, `geopolitical_sources` | Sourced maritime, sanctions and conflict-zone event history | macro-research |
| `plot_visual_artifact`, `release_calendar_visual_artifact` | Charts and the calendar view; table fallback when Apps cannot render | all research workflows |
| `macro_briefing_task`, `macro_heatmap_task` | Multi-step briefing and heatmap outputs | macro-brief / macro-research |
| `event_impact_replay_task`, `fx_backtest_task`, `fx_trade_setup_task` | Release replays, spot FX backtests and research trade setups | release-context / macro-research |
| `research_run_*`, `research_paper_*` | A signed-in subscriber's own saved research studies and simulated paper accounts | macro-research |

## What the tools can change

Data tools are read-only. The `research_run_*` and `research_paper_*` tools save, pause, archive or cancel only the signed-in subscriber's own research studies and simulated paper accounts. No tool places live orders, moves money or changes account settings.

## Transport boundaries

This is a native MCP plugin, not a REST client. It does not expose a separate alias for every REST path, and it does not consume the continuous event stream. Use a suitable REST or SSE client separately when those operations are required.

MCP Apps may render visual artifacts in compatible hosts. The plugin adds no renderer or headless visual service; plain text and tables remain the fallback. Installation does not start a background watcher or create subscriptions.
