# Working Machines - Cursor Plugin Repository

Official Cursor plugin repository for [Working Machines](https://www.workingmachines.dev).

Connect Cursor to **1,400+ apps** and **15,000+ machine-ready tools remotely** through one secure, hosted Model Context Protocol (MCP) server.

<p align="center">
  <img src="plugins/working-machines/assets/logo.png" alt="Working Machines Logo" width="128" height="128" />
</p>

---

## Remote Access to 1,400+ Apps & 15,000+ Tools

Working Machines provides the application layer for AI agents. Through a single remote MCP connection (`https://app.workingmachines.dev/mcp`), your agent gets instant access to 1,400+ integrations and 15,000+ structured actions across:

- **Team Collaboration**: Slack, Gmail, Google Workspace, Microsoft Teams, Notion
- **Development & Cloud**: GitHub, GitLab, Sentry, Jira, AWS, Vercel, Datadog
- **Projects & Productivity**: Linear, Asana, Trello, ClickUp, Monday.com
- **Commerce & CRM**: Salesforce, HubSpot, Stripe, Shopify, Zendesk
- **Data & Analytics**: Snowflake, BigQuery, PostgreSQL, Airtable, Pinecone

---

## Safety & Security Architecture

Working Machines is engineered from the ground up for safe, enterprise-grade AI execution:

### 🛡️ 1. Your Credentials Are Not Context
- **Zero Local Secret Storage**: API keys, OAuth tokens, and secret credentials stay behind the Working Machines execution boundary.
- **Context Protection**: Credentials never enter your Cursor chat context, prompt buffers, or local workspace files.

### 🔒 2. Scoped Capabilities & Policy Enforcement
- **Intent-Based Access**: Agents discover only the minimal actions required for the task at hand rather than loading full provider schemas.
- **Provider-Native Scopes**: Connect accounts once with provider-bound permissions (e.g. create issues only).
- **Execution Policies**: Allow, reject, or require approval for actions before any call leaves the execution boundary.

### 📋 3. Verifiable & Auditable Run History
- **Structured Proof**: Every action execution produces a structured, redacted, and auditable record.
- **Execution Visibility**: Tracks who acted, which connection was used, what changed, timing, and policy decisions for complete transparency.

---

## Repository Structure

This repository follows the official Cursor plugin marketplace format:

```text
working-machines/
├── .cursor-plugin/
│   └── marketplace.json
├── plugins/
│   └── working-machines/
│       ├── .cursor-plugin/
│       │   └── plugin.json
│       ├── assets/
│       │   └── logo.png
│       ├── skills/
│       │   └── working-machines/
│       │       └── SKILL.md
│       ├── mcp.json
│       └── README.md
├── scripts/
│   └── validate-template.mjs
├── README.md
├── CHANGELOG.md
├── LICENSE
├── NOTICE
└── .gitignore
```

---

## Agent Workflow

Cursor agents follow the Working Machines discovery and execution sequence:

```text
list_apps
      ↓
list_connections
      ↓
search_actions
      ↓
get_action_guide
      ↓
execute_action
      ↓
verify result
```

1. **`list_apps`**: Discover available applications and tool integrations.
2. **`list_connections`**: Verify active account authorizations and permissions.
3. **`search_actions`**: Find machine actions by intent.
4. **`get_action_guide`**: Retrieve validated schemas and input parameters.
5. **`execute_action`**: Execute the action securely behind the boundary.
6. **Verify Result**: Audit the structured execution response.

---

## Validation

Verify repository manifest and component compliance:

```bash
node scripts/validate-template.mjs
```

---

## Documentation & Links

- **Website**: [https://www.workingmachines.dev](https://www.workingmachines.dev)
- **Documentation**: [https://www.workingmachines.dev/docs](https://www.workingmachines.dev/docs)
- **App Dashboard**: [https://app.workingmachines.dev](https://app.workingmachines.dev)

---

## License & Notice

- Open-source plugin wrapper licensed under the [MIT License](LICENSE).
- See the [NOTICE](NOTICE) file regarding proprietary hosted infrastructure details.
