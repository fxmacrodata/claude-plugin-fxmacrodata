# FXMacroData connector

The native host connects over HTTP to `https://mcp.fxmacrodata.com/mcp`. The default configuration is keyless. Tools are discovered dynamically; their connected input schemas are authoritative. The following reviewed inventory documents the plugin's workflow coverage, without freezing the server's tools or recreating their implementation.

All listed tools are available through the host's ordinary MCP tool selection. The macro-research command routes requests across them; the focused commands combine relevant tools into usable work products. Access and App rendering support vary by tool and host.

| Tool | Native workflow |
|---|---|
| `ping` | Connection/capability/access guidance when requested |
| `mcp_capabilities` | Connection/capability/access guidance when requested |
| `mcp_auth_guide` | Connection/capability/access guidance when requested |
| `subscribe_for_mcp_access` | Connection/capability/access guidance when requested |
| `data_catalogue` | macro-brief / macro-research |
| `risk_sentiment` | currency-context / macro-research |
| `risk_sentiment_changes` | Retained sentiment-change history with `after_sequence` resume cursor; currency-context / macro-research |
| `macro_news` | macro-brief / macro-research |
| `release_calendar` | release-context / macro-research |
| `release_calendar_visual_artifact` | Matching research chart; table fallback when Apps cannot render |
| `event_predictions` | release-context / macro-research |
| `latest_announcements` | release-context / macro-research |
| `announcement_changes` | release-context / macro-research |
| `press_releases` | macro-brief / macro-research |
| `macro_factor` | currency-context / macro-research |
| `fx_reference_sources` | currency-context / macro-research |
| `fx_reference_universe` | currency-context / macro-research |
| `fx_intraday_reference_rates` | currency-context / macro-research |
| `rate_curve` | currency-context / macro-research |
| `rate_differentials` | currency-context / macro-research |
| `latest_commodities` | currency-context / macro-research |
| `forex` | currency-context / macro-research |
| `seasonality` | macro-research with the connected tool's documented scope |
| `indicator_query` | macro-brief / macro-research |
| `plot_visual_artifact` | Matching research chart; table fallback when Apps cannot render |
| `indicator_visual_artifact` | Matching research chart; table fallback when Apps cannot render |
| `forex_visual_artifact` | Matching research chart; table fallback when Apps cannot render |
| `commodities_visual_artifact` | Matching research chart; table fallback when Apps cannot render |
| `cot_visual_artifact` | Matching research chart; table fallback when Apps cannot render |
| `policy_rate_differential_visual_artifact` | Matching research chart; table fallback when Apps cannot render |
| `macro_briefing_task` | macro-brief / macro-research |
| `indicator_intel_task` | macro-research with the connected tool's documented scope |
| `pair_intel_task` | macro-research with the connected tool's documented scope |
| `macro_heatmap_task` | macro-research with the connected tool's documented scope |
| `policy_scenario_modeler_task` | macro-research with the connected tool's documented scope |
| `macro_war_room_task` | macro-research with the connected tool's documented scope |
| `event_impact_replay_task` | macro-research with the connected tool's documented scope |
| `quant_scenario_lab_task` | macro-research with the connected tool's documented scope |
| `known_at_time_task` | macro-research with the connected tool's documented scope |
| `macro_regime_classifier_task` | macro-research with the connected tool's documented scope |
| `release_risk_score_task` | macro-research with the connected tool's documented scope |
| `portfolio_risk_engine_task` | macro-research with the connected tool's documented scope |
| `fx_trade_setup_task` | macro-research with the connected tool's documented scope |
| `fx_backtest_task` | macro-research with the connected tool's documented scope |
| `macro_research_pack_task` | macro-research with the connected tool's documented scope |
| `prediction_coverage` | release-context / macro-research |
| `market_sessions` | currency-context / macro-research |
| `cot_data` | currency-context / macro-research |
| `commodities` | currency-context / macro-research |
| `financial_prices` | currency-context / macro-research |
| `official_dataset_family` | macro-research with the connected tool's documented scope |

## Transport boundaries

This is a native MCP plugin, not a REST client. It does not expose a separate alias for every REST path. The REST-only research-panel POST, session/reference-rate variants without a matching advertised tool, health-path aliases and continuous `/v1/stream/events` are not implemented as commands. Use a suitable REST/SSE client separately when those operations are required.

MCP Apps may render visual artifacts in compatible hosts. The plugin adds no renderer or headless visual service; plain text and tables remain the fallback. Installation does not start a background watcher or create subscriptions.
