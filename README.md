# @pipeworx/data-ny

[data.ny.gov](https://data.ny.gov) MCP — New York State open-data Socrata portal. Keyless.

Part of [Pipeworx](https://pipeworx.io) — an MCP gateway connecting AI agents to 1394+ live data sources.

## Tools

- `datasets(query?, limit?, offset?)` — search dataset catalogue
- `query(resource_id, where?, select?, group?, order?, limit?, offset?)` — SoQL query on a single resource
- `metadata(resource_id)` — resource metadata
- `column_data(resource_id, column)` — distinct values in a column

`resource_id` is the 4x4 (e.g. `xj2p-gjci`).

## Data source

`https://data.ny.gov/resource/<id>.json` (Socrata SODA 2.1).

## Quick Start

Add to your MCP client (Claude Desktop, Cursor, Windsurf, etc.):

```json
{
  "mcpServers": {
    "data-ny": {
      "url": "https://gateway.pipeworx.io/data-ny/mcp"
    }
  }
}
```

Or connect to the full Pipeworx gateway for access to all 1394+ data sources:

```json
{
  "mcpServers": {
    "pipeworx": {
      "url": "https://gateway.pipeworx.io/mcp"
    }
  }
}
```

## Using with ask_pipeworx

Instead of calling tools directly, you can ask questions in plain English:

```
ask_pipeworx({ question: "your question about Data Ny data" })
```

The gateway picks the right tool and fills the arguments automatically.

## More

- [Docs and guides](https://pipeworx.io/docs)
- [pipeworx.io](https://pipeworx.io)

## License

MIT
