# Workspace Management

Tools for looking up information about your team (workspace).

### get\_channels

**Read** · List all channels in your team (WhatsApp, WhatsApp Business API, Messenger and Instagram) with their UUIDs, names, types, connection status and phone number or page/account ID. The assistant uses this to find the `channel_uuid` that most other tools need, so you can refer to a channel by its name or number, e.g. *"in the Sales channel"*.

**Example prompt:** *"Which channels do we have, and are they all connected?"*

This tool takes no parameters.

| Field returned | Description |
| --- | --- |
| `uuid` | The channel's `channel_uuid` |
| `name` | Channel name |
| `type` | `whatsapp`, `waba`, `messenger` or `instagram` |
| `status` | Connection status, e.g. `ready` or `disconnected` |
| `contact_number` | The channel's own phone number, or its page/account ID for Messenger and Instagram |

### get\_team\_staff

**Read** · List the members of your team with their IDs, names, emails and roles. The assistant uses this to turn a name like *"Sarah"* into the `staff_id` needed for [assigning](contact-management.md#assign_assignee_to_contact) or [adding collaborators](contact-management.md#add_collaborator_to_contact).

**Example prompt:** *"Show me all team members."*

| Parameter | Required | Description |
| --- | --- | --- |
| `search` | No | Search by name or email, min 2 characters |
| `role` | No | Filter by role, e.g. `admin` |
| `sort` | No | `name` (default), `email`, `created_at`, `last_login` or `role` |
| `order` | No | `asc` (default) or `desc` |
| `page` / `per_page` | No | Pagination (default 50 per page, max 100) |

{% hint style="success" %}
`get_channels` and `get_team_staff` are good first tools to test your MCP connection. They are read-only and need no Channel UUID.
{% endhint %}
