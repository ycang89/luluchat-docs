# Settings: AI

## What is AI Settings?
Enable and configure AI-powered features, including Model Control Protocol (MCP) for advanced tool automation.

## How to set it up (Step by Step)

### Step 1: Enable MCP
Toggle **Enable MCP for AI** to "On" to allow AI agents to use external tools and advanced logic.

📸 Screenshot placeholder:
> [Screenshot: MCP for AI toggle switch]

### Step 2: Retrieve Connectivity Info
Once enabled, you will see your **MCP Server URL**.
- *Note*: You will also need an **MCP Token**, which must be generated in the [Integration](../account/integration.md) tab.

📸 Screenshot placeholder:
> [Screenshot: MCP Server URL display]

### Step 3: Manage Tool Permissions
AI agents can be restricted to specific tools. Use the **MCP Tool Permissions** list to toggle individual capabilities on or off.
- **Enable All**: Grants the agent access to every available tool.
- **Disable All**: Strips all tool permissions.

📸 Screenshot placeholder:
> [Screenshot: List of tool permissions with Enable/Disable All buttons]

## Important behavior to know
- **MCP for Advanced Flows**: MCP is required if you want your AI agent to perform actions like checking databases or calling external APIs during a conversation.
- **Token Requirement**: AI features will not function until a valid token is generated and configured.

## Best practice 💡
- **Least Privilege**: Only enable the specific tool permissions an AI agent needs for its current objective.
- **Test Objective**: Verify AI behavior in a test flow after changing permissions.
