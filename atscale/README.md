# AtScale for Cursor

Ground Cursor's AI agent in your [AtScale](https://www.atscale.com) semantic layer so it reasons over governed metrics and trusted business definitions, not raw tables.

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
