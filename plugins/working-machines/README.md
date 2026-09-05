# Working Machines MCP Server Plugin for Cursor

Official Cursor plugin for [Working Machines](https://www.workingmachines.dev).

See the [Cursor integration guide](https://www.workingmachines.dev/agents/cursor) for setup, workflow examples, and security boundaries.

Connect Cursor remotely to **1,400+ apps** and **15,000+ machine-ready actions** through one secure, hosted Model Context Protocol (MCP) server.

<p align="center">
  <img src="assets/logo.png" alt="Working Machines Logo" width="128" height="128" />
</p>

---

## Capabilities

- **1,400+ Apps & 15,000+ Tools**: Seamless access to GitHub, Slack, Jira, Sentry, Salesforce, Linear, Gmail, Notion, Stripe, and 1,400+ more integrations.
- **Remote MCP Server**: Zero local infrastructure setup. Connects directly to `https://app.workingmachines.dev/mcp`.

## Safety & Security Features

- **Credentials Are Not Context**: OAuth tokens and API keys remain behind Working Machines' secure execution boundary and never enter agent context or local files.
- **Scoped Permissions & RBAC**: Tasks request intent-based actions with provider-native scopes attached.
- **Auditable Executions**: Every call returns structured, verifiable run records for complete governance.

---

## Configuration

- **MCP Endpoint**: Configured in `mcp.json` (`https://app.workingmachines.dev/mcp`).
- **Agent Skill**: Defined in `skills/working-machines/SKILL.md`.
