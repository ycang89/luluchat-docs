# AI

## What is AI Settings?

AI Settings allow you to enable and configure AI-powered features for your workspace, including Model Control Protocol (MCP) which lets AI agents use advanced automation tools.

## When does it trigger?

These settings take effect whenever a contact interacts with an **AI Agent node** in your Message Flows. The AI agent's capabilities and permissions are determined by what you configure here.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Access AI Settings

Go to `Settings` in the left menu, then navigate to Tools > AI.

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-13 at 3.31.35 PM.png" alt=""><figcaption></figcaption></figure>

> \[Screenshot: Settings menu with Tools > AI highlighted]
{% endstep %}

{% step %}
#### Enable MCP

Toggle Enable MCP for AI to "On" to allow your AI agents to perform complex tasks like checking databases or calling external APIs. Use the MCP Tool Permissions list to specifically enable or disable what the AI agent can do. Use Enable All or Disable All for quick management.

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-13 at 3.31.35 PM (1).png" alt=""><figcaption></figcaption></figure>

> \[Screenshot: MCP for AI toggle switch set to ON]
{% endstep %}

{% step %}
#### Create MCP Token

You will also need an MCP Token, which you can generate in the `Settings > Account > Integration` tab. You will need this for your AI service provider.

<div><figure><img src="../../.gitbook/assets/Screenshot 2026-02-13 at 3.34.07 PM.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/Screenshot 2026-02-13 at 3.34.45 PM.png" alt=""><figcaption></figcaption></figure></div>

> \[Screenshot: Create token for MCP]
{% endstep %}

{% step %}
#### Configure MCP Server URL

[https://mcp.luluchat.io/mcp](https://mcp.luluchat.io/mcp) will be your MCP Server URL, pass it to your AI service provider.
{% endstep %}
{% endstepper %}

## What happens after it triggers?

Once configured, your AI agents will be able to provide more relevant, data-driven responses. If a tool permission is granted, the AI can "call" that tool to perform a specific action during a live chat.

## Important behavior to know

* **Advanced Flows Only**: AI Agents and MCP are typically used in complex conversation paths where standard "If/Else" logic isn't enough.
* **Token Security**: Your MCP token is sensitive. Do not share it with anyone outside your trusted administration team.
* **Integration Required**: AI features require a valid API key from **Praxus AI** to function.

## Common issues & solutions

* **AI Agent not responding**: Check if the "Enable MCP for AI" toggle is on and verify that your API key in the Integration tab is valid.
* **Permission Denied errors**: If the AI tries to perform an action but fails, ensure that specific tool is enabled in your **MCP Tool Permissions** list.

## Best practice 💡

* **Least Privilege**: Only enable the specific tool permissions an AI agent needs. This makes the agent faster and more reliable.
* **Test Before Launch**: Always test your AI-powered flows with a test contact to ensure the agent follows your instructions correctly.
