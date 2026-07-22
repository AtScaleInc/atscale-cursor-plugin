# AtScale for Cursor

Empower Cursor's AI agent with governed metrics and trusted business definitions for ALL of your enterprise data with [AtScale](https://www.atscale.com)'s Universal Semantic Layer.

## Prerequisites

- An AtScale deployment with the MCP server enabled.
  - The server should be reachable via `https://<your-atscale-domain>/mcp`.
- OAuth access to that AtScale instance.

## Setup

The plugin requires two environment variables to authenticate with OAuth:

- `ATSCALE_MCP_URL` (e.g., `https://your-atscale-domain/mcp`)
- `ATSCALE_MCP_CLIENT_ID`
  - This is the secret for the `atscale-mcp` client. You can find it by going to your AtScale instance's Keycloak page > Clients > `atscale-mcp` > Credentials. 

Set these in your path, e.g. by setting the following in `.zshrc`:

```
export ATSCALE_MCP_URL=https://<your-atscale-domain>/mcp
export ATSCALE_MCP_CLIENT_SECRET=<your-atscale-secret>
```

then fully restart Cursor so it inherits the new values. 

From the "Customize" tab in Cursor, add AtScale's plugin via the marketplace and authenticate.
