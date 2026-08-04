# AtScale for Cursor

Empower Cursor's AI agent with governed metrics and trusted business definitions for ALL of your enterprise data with [AtScale](https://www.atscale.com)'s Universal Semantic Layer.

## Prerequisites

- An AtScale deployment with the MCP server enabled.
  - The server should be reachable via `https://<your-atscale-domain>/mcp`.
- OAuth access to that AtScale instance.

## Setup

In Cursor Desktop, add the AtScale plugin via the Customize tab.

Select the plugin, then click Configure in the top right corner of the app. Fill in the necessary fields, then click Save.

> If the "Configure" option isn't available, you can also set the `ATSCALE_MCP_URL` and `ATSCALE_MCP_CLIENT_SECRET` variables in your environment. Once you do so, quit Cursor, restart, and try to authenticate.

Once you authenticate the MCP, you're ready to use the plugin. 
