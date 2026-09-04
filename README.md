# Working Machines - Cursor Plugin Repository

Official Cursor plugin repository for [Working Machines](https://www.workingmachines.dev).

Connect Cursor to **1,400+ apps** and **15,000+ machine-ready actions** through a secure, remote Model Context Protocol (MCP) server.

<p align="center">
  <img src="plugins/working-machines/assets/logo.png" alt="Working Machines Logo" width="128" height="128" />
</p>

---

## Repository Structure

This repository is structured according to the official Cursor plugin marketplace template:

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

## How It Works

Cursor agents equipped with the Working Machines plugin follow this discovery and execution model:

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

1. **`list_apps`**: Discover supported third-party application integrations.
2. **`list_connections`**: Check active user authentications.
3. **`search_actions`**: Find relevant machine-ready actions.
4. **`get_action_guide`**: Retrieve action schema and execution parameter guides.
5. **`execute_action`**: Execute the action securely.
6. **Verify Result**: Inspect execution outputs and return feedback to the user.

---

## Validation & Quality Checks

Run the template validator to verify manifest and component compliance:

```bash
node scripts/validate-template.mjs
```

---

## Documentation & Support

- **Documentation**: [https://www.workingmachines.dev/docs](https://www.workingmachines.dev/docs)
- **App Dashboard**: [https://app.workingmachines.dev](https://app.workingmachines.dev)

---

## License & Notice

- This wrapper repository is licensed under the [MIT License](LICENSE).
- See the [NOTICE](NOTICE) file for proprietary details regarding Working Machines backend infrastructure and services.
