# FXMacroData plugin for Claude

[FXMacroData](https://fxmacrodata.com/?utm_source=github&utm_medium=referral&utm_campaign=claude-plugin-fxmacrodata) provides official-source FX, macroeconomic and central-bank data inside Claude Code: release calendars,
indicator histories, policy rates, FX spot rates, COT positioning and commodities across 22
currencies.

## Install

```
/plugin marketplace add fxmacrodata/claude-plugin-fxmacrodata
/plugin install fxmacrodata@fxmacrodata
```

## What's included

- **MCP server**: the hosted FXMacroData server at `https://mcp.fxmacrodata.com/mcp`.
- **Skill**: guides Claude to pick the right FXMacroData tool for macro and FX questions.
- **Commands**:
  - `/fxmacrodata:macro-brief USD` - policy rate, inflation, jobs, growth and the next releases.
  - `/fxmacrodata:pair-brief EURUSD` - rate differential, inflation gap, spot and event risk.

## Access

USD data works without an account. Other currencies, FX rates, COT, commodities and research
tools need an FXMacroData subscription. Run `/mcp` in Claude Code and choose **fxmacrodata** to
sign in.

Pricing: https://fxmacrodata.com/subscribe?utm_source=github&utm_medium=referral&utm_campaign=claude-plugin-fxmacrodata

## Example prompts

- "What US data is due this week?"
- "Show me the last 12 months of US core CPI."
- "How has the Fed funds rate moved this year?"

## Support

- Documentation: https://fxmacrodata.com/documentation/mcp-server?utm_source=github&utm_medium=referral&utm_campaign=claude-plugin-fxmacrodata
- Email: info@fxmacrodata.com
- Privacy policy: https://fxmacrodata.com/privacy
- Terms: https://fxmacrodata.com/terms

## License

MIT
