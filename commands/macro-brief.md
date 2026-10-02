---
description: Macro briefing for a currency - policy rate, inflation, jobs, growth and the next scheduled releases
argument-hint: <currency, e.g. USD>
---

Build a concise macro briefing for $ARGUMENTS using the FXMacroData tools.

1. Call `data_catalogue` for the currency to get the indicator slugs.
2. Pull the latest policy rate, headline and core inflation, unemployment and GDP with
   `indicator_query`.
3. Call `release_calendar` for the next scheduled releases.
4. Summarise in under 200 words: current stance, the latest prints with their release dates, and
   what is due next. If a currency needs a subscription, say so and include the subscribe link
   from the tool result.
