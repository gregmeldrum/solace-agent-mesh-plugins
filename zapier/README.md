# zapier SAM Plugin

A SAM agent for interacting with Zapier tools

[Zapier](https://zapier.com/)

This is a plugin for Solace Agent Mesh (SAM).

## Configuration (`config.yaml`)

The `config.yaml` in this plugin serves as a template. When you use `sam plugin add <component_name> --plugin zapier`, the following placeholders in the YAML structure will be replaced with variations of `<component_name>`:
- `__COMPONENT_UPPER_SNAKE_CASE_NAME__`
- `__COMPONENT_KEBAB_CASE_NAME__`
- `__COMPONENT_PASCAL_CASE_NAME__`

Customize the `config.yaml` in this plugin directory to define the base configuration for components created from it.

## Usage
1. Launch SAM plugin catalog `sam plugin catalog` 
2. Add this repository to your SAM instance if you have not done so already.  `+ Add Registry`, paste in the git repository [https://github.com/solacecommunity/solace-agent-mesh-plugins](https://github.com/solacecommunity/solace-agent-mesh-plugins) with name `Community`
3. Install the Zapier agent using the install button in the gui or with `sam plugin add zapier --plugin zapier`
4. Supply your Zapier mcp server token as `export ZAPIER_TOKEN="your_api_key_here"`

You will need a Zapier MCP server with tools exposed [Zapier MCP](https://mcp.zapier.com/)

To use the Tavily agent in SAM you will have to ask the orchestrator to find some information on the web and do something with it. 