---
description: Review scheduled macro releases and recent publication or revision changes
argument-hint: "[currency, default USD] [indicator or event]"
---

# Release context

Use the research-provenance skill. Resolve the currency and requested indicator through `data_catalogue`; default to USD.

1. Retrieve `release_calendar` for the selected scope. Display the exact returned scheduled time, timezone and any qualification; do not infer an event from release cadence.
2. Use `latest_announcements` and, if available, `announcement_changes` to distinguish newly released observations from revisions. Preserve any returned cursor. A single limited page is not a complete revision history.
3. For a named event, use `indicator_query` to retrieve comparable prior observations. Where available, `event_predictions` and `prediction_coverage` add forecast context; put forecasts in separate columns and retain their source and generation metadata.
4. Use `event_impact_replay_task` or `release_risk_score_task` only if the question requests those analyses and the connected schema supports the requested scope. These are research outputs, not execution instructions.
5. Produce a release table with period, value, scheduled time, observed publication evidence, revision status, source and unknown fields. Treat unknown publication time as unknown. Do not equate a capture time with publisher publication time.

This command is an interactive snapshot. It does not register a webhook, start unattended monitoring or subscribe to a continuous SSE stream.
