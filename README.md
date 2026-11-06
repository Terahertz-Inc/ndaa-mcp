# NDAA.AI MCP Server: FY2027 NDAA tracker for AI agents

[Model Context Protocol](https://modelcontextprotocol.io) (MCP) server for [NDAA.AI](https://ndaa.ai), the public tracker for the FY2027 National Defense Authorization Act (H.R. 8800 / S. 4784). Get bill status, section text, House vs Senate differences and NDAA news in Claude, Cursor or any MCP client, with ndaa.ai links to cite.

**Website:** [ndaa.ai](https://ndaa.ai) · **MCP page:** [ndaa.ai/mcp](https://ndaa.ai/mcp)

| | |
|---|---|
| Endpoint | `https://mcp.ndaa.ai/mcp` |
| Transport | Streamable HTTP |
| Auth | None. Public, read-only |
| npm (stdio) | [`ndaa-mcp`](https://www.npmjs.com/package/ndaa-mcp) |
| Registry name | `ai.ndaa/mcp` (see [`server.json`](server.json)) |

## Tools

| Tool | What it does |
|---|---|
| `get_status` | Current FY2027 NDAA bill status: headline, summary, next steps, stage tracker and as-of date |
| `search_sections` | Search NDAA sections by keyword or topic (pay raise, FOCI, OTA, shipbuilding, etc.) |
| `get_section` | One section: plain-language summary, statutory text, and House and Senate variants |
| `compare_house_senate` | Compare House (H.R. 8800) and Senate (S. 4784) text for a section or topic |
| `latest_news` | Latest NDAA news tracked on ndaa.ai, with outlet, date, summary and source |
| `list_updates` | Dated NDAA update posts, newest first |
| `get_update` | One dated update post with every story and its source |
| `list_guides` | NDAA.AI explainer guides (status, House vs Senate, FY2027 vs FY2026, military pay raise) |

## Install

### Remote (Claude custom connector, Cursor, any Streamable HTTP client)

```json
{
  "mcpServers": {
    "ndaa": { "url": "https://mcp.ndaa.ai/mcp" }
  }
}
```

### Stdio (Claude Desktop and other stdio clients)

```json
{
  "mcpServers": {
    "ndaa": { "command": "npx", "args": ["-y", "ndaa-mcp"] }
  }
}
```

### Muse

```json
{
  "mcpServers": {
    "ndaa": { "transport": "streamable_http", "url": "https://mcp.ndaa.ai/mcp" }
  }
}
```

## Example prompts

- "Where is the FY2027 NDAA right now?"
- "What military pay raise is in the House and Senate NDAA bills?"
- "Compare the House and Senate shipbuilding sections."
- "What's the latest NDAA news this week?"

## Links

- [ndaa.ai](https://ndaa.ai) · [MCP page](https://ndaa.ai/mcp)
- [npm package](https://www.npmjs.com/package/ndaa-mcp) · [Issues](../../issues)

## License

[MIT](LICENSE) © Terahertz, Inc.
