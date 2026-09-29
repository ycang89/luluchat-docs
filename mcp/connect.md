# Connect with an Access Token

## What is it?

To connect an AI assistant to Luluchat, you need two things:

| Item | Value |
| --- | --- |
| **MCP Server URL** | `https://mcp.luluchat.io/mcp` |
| **Access Token** | A token you create in `Settings > Account > Integration` |

Your AI assistant sends the access token with every request in the `Authorization` header:

```
Authorization: Bearer YOUR_ACCESS_TOKEN
```

This page shows how to create the token and add it to popular AI apps.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Enable MCP for AI

1. Go to `Settings` in the left menu, then **Tools > AI**
2. Turn **Enable MCP for AI** to **On**
3. Under **MCP Tool Permissions**, turn on the tools you want the AI to use (or click **Turn On All**)
4. Click **Save**

See [AI Settings](../settings/tools/ai.md) for more details.
{% endstep %}

{% step %}
#### Create an MCP Access Token

1. Go to `Settings > Account >` [**Integration**](https://app.luluchat.io/settings?view=integration)
2. In the **Access Token** section, click **Create Access Token**
3. Fill in the form:
   * **Name**: A name that helps you remember where it's used, e.g. `Claude Desktop - Sales Team`
   * **Expiry**: 1, 3, 6 or 12 months, or **Never**
   * **Scopes**: Tick **All MCP Tool Scopes**
4. Click **Submit**
5. Copy the token from the **Access Token Created Successfully** window

{% hint style="danger" %}
The token is **only shown once**. Copy it and keep it somewhere safe. If you lose it, delete the token and create a new one.
{% endhint %}
{% endstep %}

{% step %}
#### Find your Channel UUID

Most tools need a **Channel UUID** to know which WhatsApp channel to work with.

1. Click the **Channels** button in the header bar
2. Each channel card shows `ID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx`
3. Click the copy icon next to it

{% hint style="success" %}
**Tip:** Tell the assistant your Channel UUID once, e.g. put it in the assistant's instructions or project prompt: *"My Luluchat channel\_uuid is 550e8400-e29b-41d4-a716-446655440000."* Then you don't need to repeat it in every request.
{% endhint %}
{% endstep %}

{% step %}
#### Add Luluchat to your AI assistant

Pick your app below and replace `YOUR_ACCESS_TOKEN` with the token you copied.
{% endstep %}
{% endstepper %}

## Connect your AI assistant

{% tabs %}
{% tab title="Claude Code" %}
Run this command in your terminal:

```bash
claude mcp add --transport http luluchat https://mcp.luluchat.io/mcp \
  --header "Authorization: Bearer YOUR_ACCESS_TOKEN"
```

Then start Claude Code and type `/mcp` to check that **luluchat** is connected.
{% endtab %}

{% tab title="Claude Desktop" %}
1. Open Claude Desktop, go to **Settings > Developer**, and click **Edit Config**
2. Add Luluchat to `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "luluchat": {
      "command": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://mcp.luluchat.io/mcp",
        "--header",
        "Authorization:${LULUCHAT_AUTH}"
      ],
      "env": {
        "LULUCHAT_AUTH": "Bearer YOUR_ACCESS_TOKEN"
      }
    }
  }
}
```

3. Save the file and restart Claude Desktop

{% hint style="info" %}
This setup uses `mcp-remote` to pass your token, so [Node.js](https://nodejs.org) must be installed on your computer.
{% endhint %}
{% endtab %}

{% tab title="Cursor" %}
Open **Cursor Settings > MCP > Add new global MCP server**, or edit `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "luluchat": {
      "url": "https://mcp.luluchat.io/mcp",
      "headers": {
        "Authorization": "Bearer YOUR_ACCESS_TOKEN"
      }
    }
  }
}
```

Save the file. **luluchat** should show a green dot in the MCP settings.
{% endtab %}

{% tab title="VS Code" %}
Create `.vscode/mcp.json` in your project (or run **MCP: Add Server** from the Command Palette):

```json
{
  "servers": {
    "luluchat": {
      "type": "http",
      "url": "https://mcp.luluchat.io/mcp",
      "headers": {
        "Authorization": "Bearer YOUR_ACCESS_TOKEN"
      }
    }
  }
}
```

Then open Copilot Chat in **Agent** mode. The Luluchat tools appear in the tools list.
{% endtab %}

{% tab title="Other apps / Custom agent" %}
Any AI platform or agent framework that supports **remote MCP servers (Streamable HTTP)** with custom headers can connect to Luluchat.

Use these settings:

* **Server URL**: `https://mcp.luluchat.io/mcp`
* **Transport**: Streamable HTTP
* **Header name**: `Authorization`
* **Header value**: `Bearer YOUR_ACCESS_TOKEN`

Look for a setting called *MCP Server*, *Connector*, *Custom tool* or *Integration* in your AI platform.
{% endtab %}
{% endtabs %}

## Test the connection

Ask your assistant something simple and read-only, for example:

> "Using Luluchat, show me all my team members."

The assistant should call the `get_team_staff` tool and list your team. If it does, you're connected! 🎉

Next, browse the [Available Tools](tools/index.md) to see everything the assistant can do.

## Important behavior to know

* **Bearer format**: The header value must be `Bearer` + a space + your token. Sending the token without `Bearer` will be rejected.
* **Token expiry**: When a token expires, the assistant loses access. Create a new token and update your assistant's settings.
* **Deleting a token**: Deleting a token in the Access Token table immediately disconnects every assistant using it.
* **One token per app**: Create a separate token for each app or person. You can then remove access for one app without affecting the others.
* **Last Used**: The Access Token table shows when each token was last used, so you can spot tokens that are no longer needed.

## Common issues & solutions

* **401 / Unauthorized**: The token is wrong, expired or deleted, or the header is missing the `Bearer ` prefix. Create a new token and try again.
* **Token has no MCP access**: The token was created without **All MCP Tool Scopes**. Create a new token with that scope ticked.
* **Assistant says a tool is not available / permission denied**: The tool is turned off. Go to `Settings > Tools > AI`, turn it on under **MCP Tool Permissions** and click **Save**.
* **No tools at all**: Make sure **Enable MCP for AI** is turned on in `Settings > Tools > AI`.
* **channel\_access\_denied**: The Channel UUID is wrong or belongs to another team. Copy it again from the **Channels** modal.
* **contact\_not\_found**: The contact doesn't exist in that channel. Check the phone number includes the country code, e.g. `+60123456789`.
* **Claude Desktop doesn't show Luluchat**: Check the JSON is valid, Node.js is installed, and fully quit and reopen Claude Desktop.

## Best practice 💡

* **Name tokens clearly** so you know which app uses which token.
* **Set an expiry** instead of **Never** for tokens used in testing.
* **Never paste your token** into a chat message, screenshot or shared document.
* **Review tool permissions** regularly and turn off tools you no longer use.
