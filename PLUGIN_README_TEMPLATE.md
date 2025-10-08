# [Plugin Name] SAM Plugin

<!-- Brief one-line description of what this plugin does -->
[Brief description of the plugin's primary functionality]

<!-- Link to external service/API documentation if applicable -->
[Link to service documentation](https://example.com/)

---

**Plugin Type:** `[Wrapper Agent | Custom Code Agent | Gateway]`

> **Note:** This is a community-contributed plugin for [Solace Agent Mesh (SAM)](https://solacelabs.github.io/solace-agent-mesh/) and is not officially supported by Solace. For community support, please open an issue in this repository.

---

## Overview

<!-- Provide 2-3 paragraphs describing what the plugin does, its use cases, and how it fits into SAM -->
[Detailed description of the plugin, including its purpose, capabilities, and typical use cases within SAM]

## Features

<!-- List the key features and capabilities this plugin provides -->
This agent provides the following capabilities:

- **Feature 1**: [Description]
- **Feature 2**: [Description]
- **Feature 3**: [Description]

## Configuration

<!-- Describe required environment variables, API keys, or config.yaml settings -->
The plugin requires the following environment variables to be set:

- `VARIABLE_NAME`: [Description of what this variable is for]
- `ANOTHER_VARIABLE`: [Description]

### Configuration File (`config.yaml`)

<!-- Optional: Include if the config.yaml has special considerations -->
The `config.yaml` in this plugin serves as a template. When you use `sam plugin add <component_name> --plugin [plugin-name]`, the following placeholders in the YAML structure will be replaced with variations of `<component_name>`:
- `__COMPONENT_UPPER_SNAKE_CASE_NAME__`
- `__COMPONENT_KEBAB_CASE_NAME__`
- `__COMPONENT_PASCAL_CASE_NAME__`

Customize the `config.yaml` in this plugin directory to define the base configuration for components created from it.

## Installation

To add this plugin to your SAM project, run the following command:

```bash
sam plugin add <your-new-component-name> --plugin git+https://github.com/solacecommunity/solace-agent-mesh-plugins#subdirectory=[plugin-directory-name]
```

This will create a new component configuration at `configs/plugins/<your-new-component-name-kebab-case>.yaml`.

Alternatively, you can install via the SAM Plugin Catalog:

1. Launch SAM plugin catalog: `sam plugin catalog`
2. Add this repository to your SAM instance if you have not done so already: `+ Add Registry`, paste in the git repository [https://github.com/solacecommunity/solace-agent-mesh-plugins](https://github.com/solacecommunity/solace-agent-mesh-plugins) with name `Community`
3. Install the plugin using the install button in the GUI or with: `sam plugin add [component-name] --plugin [plugin-name]`
4. Configure required environment variables (see Configuration section above)

## Usage

<!-- Provide instructions on how to use the plugin, including example prompts or commands -->
Once the agent is running, you can interact with it through the SAM orchestrator using natural language prompts.

### Example Prompts

<!-- Include 3-5 example prompts that demonstrate typical usage -->
- *"[Example user prompt 1]"*
- *"[Example user prompt 2]"*
- *"[Example user prompt 3]"*

### Tools Available

<!-- Optional: List the specific tools/functions this agent exposes, if applicable -->
The agent includes the following tools:

- **`tool_name`**: [Description of what this tool does]
- **`another_tool`**: [Description]

## External Services

<!-- Document any external APIs or services this plugin depends on -->
This plugin utilizes the following external service(s):

- **[Service Name](https://example.com/)**: [Description of what the service provides]
- **API Requirements**: [Free tier available / API key required / etc.]

## Limitations

<!-- Optional: Document any known limitations, rate limits, or constraints -->
- [Limitation 1]
- [Limitation 2]
- [Limitation 3]


## Building and Running Custom Code Agents

<!-- Optional section: Only include this section for Custom Code Agents that require additional build/run steps -->
<!-- Remove this section entirely for Wrapper Agents or Gateway plugins -->

### Prerequisites

[List any prerequisites like Python version, Node.js, dependencies, etc.]

### Build Instructions

```bash
# Example build commands
[build commands here]
```

### Running the Agent

```bash
# Example run commands
[run commands here]
```

### Development

<!-- Optional: Include development-specific instructions -->
For local development:

```bash
# Example development setup
[development commands here]
```

### Testing

<!-- Optional: Include if tests are available -->
```bash
# Example test commands
[test commands here]
```
--- 

## Original Author

<!-- Credit the original creator(s) of this plugin -->
Created by [Author Name](https://github.com/username)

## Contributing

To contribute to this plugin review [Contributing](/CONTRIBUTING.md)


---

## Changelog

### Version [X.Y.Z]
- [Change description]
- [Change description]

### Version [X.Y.Z]
- [Change description]
