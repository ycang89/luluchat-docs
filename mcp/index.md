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

Go to `Settings` > `Tools` > `MCP` and turn on **Enable MCP for AI**. Here you also choose which tools the AI may use. See [MCP Settings](../settings/tools/ai.md).
{% endstep %}

{% step %}
#### Choose how the AI app signs in

* **OAuth Client**: for Claude, Claude Code and other apps that support OAuth. Copy the **Client ID** and generate a **Client Secret** in `Settings` > `Tools` > `MCP`. See [Connect with OAuth](connect-oauth.md).
* **Access Token**: for apps without OAuth, scripts and agents. Create a token with **All MCP Tool Scopes** in `Settings` > `Account Management` > `Integration`. See [Connect with an Access Token](connect.md).
{% endstep %}

{% step %}
#### Connect your AI assistant

Add the MCP Server URL and your OAuth Client details or access token to your AI assistant, then follow the step-by-step guide for your app.
{% endstep %}
{% endstepper %}

## In this section

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Connect with OAuth</strong></td><td>Connect Claude, Claude Code and other OAuth apps with a Client ID and Client Secret, no token to paste</td><td><a href="connect-oauth.md">connect-oauth.md</a></td></tr><tr><td><strong>Connect with an Access Token</strong></td><td>Create a token and connect Claude Code, Claude Desktop, Cursor, VS Code or your own AI agent</td><td><a href="connect.md">connect.md</a></td></tr><tr><td><strong>Available Tools</strong></td><td>Every tool the Luluchat MCP Server provides, grouped by feature</td><td><a href="tools/index.md">index.md</a></td></tr></tbody></table>

## Important behavior to know

* **Workspace scoped**: The OAuth Client and access tokens belong to one team (workspace). The AI can only see and change data in that team.
* **Tool permissions apply**: If a tool is turned off in `Settings` > `Tools` > `MCP`, the AI cannot use it, even with a valid token or OAuth connection.
* **Actions are real**: Changes made by the AI (tags, tickets, deals, opt-outs) are saved to your workspace the same as if a team member did them.
* **Notes are attributed to the AI**: Internal notes created through MCP show the author **AI Agent (Tools)**.

## Best practice 💡

* **Start read-only**: When first testing, turn on only the `get_...` tools. Turn on tools that make changes once you trust the setup.
* **Least privilege**: Only turn on the tools your assistant actually needs.
* **Protect your token**: Treat the MCP access token like a password. Never share it publicly or save it in a code repository.
