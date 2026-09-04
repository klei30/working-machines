---
name: working-machines
description: Connect Cursor to 1,400+ apps and 15,000+ machine-ready actions via Working Machines hosted MCP.
---

# Working Machines Skill

Working Machines provides the application layer for AI agents, connecting Cursor to 1,400+ apps and 15,000+ machine-ready actions.

## Execution Workflow

When fulfilling a user request that involves external application tools or automations, follow this sequential discovery and execution model:

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

### Step 1: Discover Applications (`list_apps`)
Query available application integrations to check supported services and capabilities.

### Step 2: Check Connections (`list_connections`)
Verify existing user authorizations and active connections for the required application. If authentication is missing, prompt the user to authorize the application via the Working Machines dashboard.

### Step 3: Search Actions (`search_actions`)
Find specific machine actions matching the requested task (e.g., searching for GitHub issue creation, Slack messaging, Jira ticket update, database queries).

### Step 4: Fetch Action Guide (`get_action_guide`)
Retrieve parameters, required input schemas, and usage guidelines for the selected action to ensure payload correctness before invocation.

### Step 5: Execute Action (`execute_action`)
Invoke `execute_action` with verified arguments and context.

### Step 6: Verify Result
Inspect the response payload from `execute_action` to confirm success or handle any errors gracefully.
