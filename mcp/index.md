# MCP Overview

## What is MCP?

**MCP (Model Context Protocol)** is an open standard that lets AI assistants connect to other apps and use them as "tools". The Luluchat MCP Server lets AI assistants like Claude, ChatGPT, Cursor or your own AI agent work directly with your Luluchat workspace. For example, an assistant can look up a contact, read a conversation, add a tag, create a ticket or move a deal to the next stage.

Instead of clicking through the Luluchat web app, you can ask your AI assistant in plain language:

> "Tag +60123456789 as VIP Customer and assign the contact to Sarah."

The assistant picks the right Luluchat tools and runs them for you.

{% hint style="info" %}
**Luluchat MCP Server URL**

```
https://mcp.luluchat.io/mcp
```
{% endhint %}

## When to use it?

* When you want an **AI assistant** (Claude, ChatGPT, Cursor, etc.) to read or update your Luluchat data for you
* When you are building your **own AI agent** and want it to manage contacts, tickets, deals or bookings in Luluchat
* When you want **AI-powered automation** that goes beyond fixed message flow rules

## What you need

{% stepper %}
{% step %}
#### Turn on MCP for your workspace

Go to `Settings > Tools > AI` and turn on **Enable MCP for AI**. Here you also choose which tools the AI may use. See [AI Settings](../settings/tools/ai.md).
{% endstep %}

{% step %}
#### Create an MCP Access Token

Go to `Settings > Account > Integration` and create an access token with the **All MCP Tool Scopes** permission.
{% endstep %}

{% step %}
#### Connect your AI assistant

Add the MCP Server URL and your access token to your AI assistant. Follow [Connect with an Access Token](connect.md) for step-by-step setup for each app.
{% endstep %}
{% endstepper %}

## In this section

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Connect with an Access Token</strong></td><td>Create a token and connect Claude, Cursor, VS Code or your own AI agent</td><td><a href="connect.md">connect.md</a></td></tr><tr><td><strong>Available Tools</strong></td><td>Every tool the Luluchat MCP Server provides, grouped by feature</td><td><a href="tools/index.md">index.md</a></td></tr></tbody></table>

## Important behavior to know

* **Workspace scoped**: An access token belongs to one team (workspace). The AI can only see and change data in that team.
* **Tool permissions apply**: If a tool is turned off in `Settings > Tools > AI`, the AI cannot use it, even with a valid token.
* **Actions are real**: Changes made by the AI (tags, tickets, deals, opt-outs) are saved to your workspace the same as if a team member did them.
* **Notes are attributed to the AI**: Internal notes created through MCP show the author **AI Agent (Tools)**.

## Best practice 💡

* **Start read-only**: When first testing, turn on only the `get_...` tools. Turn on tools that make changes once you trust the setup.
* **Least privilege**: Only turn on the tools your assistant actually needs.
* **Protect your token**: Treat the MCP access token like a password. Never share it publicly or save it in a code repository.
