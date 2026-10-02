---
description: Macro view of an FX pair - rate differential, inflation gap, spot and upcoming event risk
argument-hint: <pair, e.g. EURUSD>
---

Build a macro view of the currency pair $ARGUMENTS using the FXMacroData tools.

1. Split the pair into base and quote currencies.
2. Get the current spot rate with `forex`.
3. Compare policy rates with `rate_differentials` and latest inflation with `indicator_query`
   for both currencies.
4. List the next high-impact releases for both currencies with `release_calendar`.
5. Summarise the macro drivers in under 200 words. Do not give trade recommendations.
