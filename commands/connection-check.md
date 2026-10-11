---
description: Check the hosted FXMacroData connection and no-key USD catalogue
argument-hint: "[optional dataset or connection question]"
disable-model-invocation: true
---

# Connection check

Use the MCP tools already provided by the host. Discover their current names and schemas; do not invent arguments or download a client. Call `ping` using its advertised schema. If the connector is missing or the call fails, report the observed failure and stop. Do not silently replace the server, change settings or start a local process.

After a successful health response, call `data_catalogue` for a bounded public USD discovery request using the actual tool schema. Confirm the returned currency, units and available metadata. Use `mcp_capabilities` only when the connection's tool or rendering support needs explanation. A successful health check does not prove access to every tool or dataset.

Return a small table for connection health, public catalogue access and any observed access limitation. Include the original error for failures without request headers, secrets or authenticated URLs. Do not query protected datasets merely to test entitlement. Keep any unavailable result unavailable.

No API key, account or payment is needed for the public USD baseline. If subscriber access is requested, use `mcp_auth_guide` for instructions and the host's private credential settings. Never ask for a key in a prompt, tool argument, shared file or screenshot. Never inspect local environment or credential files, send workspace/customer material, accept legal terms or purchase access as part of this check.
