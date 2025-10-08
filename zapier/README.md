# Zapier SAM Plugin

A SAM agent for interacting with Zapier tools to automate workflows and connect thousands of apps.

[Zapier](https://zapier.com/)

---

**Plugin Type:** `Wrapper Agent`

> **Note:** This is a community-contributed plugin for [Solace Agent Mesh (SAM)](https://solacelabs.github.io/solace-agent-mesh/) and is not officially supported by Solace. For community support, please open an issue in this repository.

---

## Overview

The Zapier plugin enables SAM to interact with Zapier's automation platform, allowing you to trigger workflows, connect to thousands of apps, and automate tasks directly from your SAM orchestrator. This wrapper agent integrates with the Zapier MCP server to expose Zapier tools within your SAM environment.

## Features

This agent provides the following capabilities:

- **App Integration**: Connect to 5,000+ apps supported by Zapier
- **Task Automation**: Automate repetitive tasks across multiple platforms
- **MCP Server Integration**: Leverages Zapier's Model Context Protocol server

## Configuration

The plugin requires the following environment variables to be set:

- `ZAPIER_TOKEN`: Your Zapier MCP server API token

### Configuration File (`config.yaml`)

The `config.yaml` in this plugin serves as a template. When you use `sam plugin add <component_name> --plugin zapier`, the following placeholders in the YAML structure will be replaced with variations of `<component_name>`:
- `__COMPONENT_UPPER_SNAKE_CASE_NAME__`
- `__COMPONENT_KEBAB_CASE_NAME__`
- `__COMPONENT_PASCAL_CASE_NAME__`

Customize the `config.yaml` in this plugin directory to define the base configuration for components created from it.

## Installation

To add this plugin to your SAM project, run the following command:

```bash
sam plugin add <your-new-component-name> --plugin git+https://github.com/solacecommunity/solace-agent-mesh-plugins#subdirectory=zapier
```

This will create a new component configuration at `configs/plugins/<your-new-component-name-kebab-case>.yaml`.

Alternatively, you can install via the SAM Plugin Catalog:

1. Launch SAM plugin catalog: `sam plugin catalog`
2. Add this repository to your SAM instance if you have not done so already: `+ Add Registry`, paste in the git repository [https://github.com/solacecommunity/solace-agent-mesh-plugins](https://github.com/solacecommunity/solace-agent-mesh-plugins) with name `Community`
3. Install the plugin using the install button in the GUI or with: `sam plugin add zapier --plugin zapier`
4. Configure required environment variables: `export ZAPIER_TOKEN="your_api_key_here"`

## Usage

Once the agent is running, you can interact with it through the SAM orchestrator using natural language prompts to trigger Zapier workflows and automation.

### Example Prompts

- *"Send a notification to Slack when this condition is met"*
- *"Add a row to my Google Sheet with this data"*

## External Services

This plugin utilizes the following external service(s):

- **[Zapier](https://zapier.com/)**: Automation platform connecting 5,000+ apps
- **[Zapier MCP Server](https://mcp.zapier.com/)**: Model Context Protocol server for Zapier integration
- **API Requirements**: Requires Zapier account and MCP server token

## Limitations

- Requires active Zapier account with MCP server access
- Available tools depend on your Zapier account configuration
- Rate limits apply based on your Zapier plan

---

## Original Author

Created by the Solace Community

## Contributing

To contribute to this plugin review [Contributing](/CONTRIBUTING.md)

---

## Changelog

### Version 0.1.0
- Initial release
- Zapier MCP server integration
- Workflow automation support
