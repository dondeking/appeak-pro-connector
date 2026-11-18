# Installing the Appeak Pro MCP server

Appeak Pro is a hosted (remote) MCP server. There is nothing to clone, build or run locally, and no API key.

- URL: `https://appeak.pro/api/mcp`
- Transport: Streamable HTTP
- Authentication: none

If the client supports remote servers, add:

```json
{
  "mcpServers": {
    "appeak-pro": {
      "type": "streamableHttp",
      "url": "https://appeak.pro/api/mcp"
    }
  }
}
```

If the client only supports local (stdio) servers, bridge it with mcp-remote:

```json
{
  "mcpServers": {
    "appeak-pro": {
      "command": "npx",
      "args": ["-y", "mcp-remote", "https://appeak.pro/api/mcp"]
    }
  }
}
```

To check it works, call `search_aso_guide` with the query "how to pick google play tags".
