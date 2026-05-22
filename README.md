# AI Agent MCP Buyer Router Template

Project MCP config and buyer-router template for teams evaluating Agent Ops Command Center.

## Use

Copy `.mcp.json` into an AI-agent workspace that supports project-scoped MCP servers.

```json
{
  "mcpServers": {
    "agent-ops-command-center": {
      "type": "stdio",
      "command": "npm",
      "args": [
        "exec",
        "--yes",
        "--package=https://github.com/ivelly42/agent-ops-command-center/releases/download/v5.142-preview/agent-ops-command-center-0.5.142.tgz",
        "--",
        "agent-ops-mcp-server"
      ],
      "env": {}
    }
  }
}
```

The MCP server exposes:

- `get_checkout_status`
- `get_team_request`
- `get_team_request_markdown`
- `get_mcp_buyer_router_template`
- `get_revenue_rule`

## Buyer Route

- Product: Agent Ops Command Center
- Offer: Team license - 7 seats - $203 gross
- Primary request: https://ivelly42.github.io/agent-ops-command-center/team-request-url.html
- Copy-ready request Markdown: `get_team_request_markdown`
- Payment-ready fallback: https://github.com/ivelly42/agent-ops-command-center/issues/new?template=payment-ready.yml
- Checkout status: https://ivelly42.github.io/agent-ops-command-center/checkout-status.json
- Metrics: https://ivelly42.github.io/agent-ops-command-center/metrics/status.json

## Revenue Rule

This template repo, MCP config loads, MCP tool calls, resource reads, generated request URLs, GitHub issues, discussions, release downloads, npm runs, stars, forks, and page views are not revenue.

Count revenue only after checkout, receipt, payout, or seller-dashboard evidence proves payment.
