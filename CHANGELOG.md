# Changelog

All notable changes to the Working Machines Cursor Plugin wrapper will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-09-05

### Added
- Customized Cursor plugin template for Working Machines.
- Marketplace manifest registration in `.cursor-plugin/marketplace.json`.
- Plugin package in `plugins/working-machines/`.
- Remote MCP server configuration pointing to `https://app.workingmachines.dev/mcp`.
- Agent skill definition in `skills/working-machines/SKILL.md` specifying the 6-step action workflow (`list_apps` -> `list_connections` -> `search_actions` -> `get_action_guide` -> `execute_action` -> verify result).
- High-resolution brand logo in `assets/logo.png`.
- Automated template validator compliance.
