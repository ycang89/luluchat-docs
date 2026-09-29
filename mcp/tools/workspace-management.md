# Workspace Management

Tools for looking up information about your team (workspace).

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
This is a good first tool to test your MCP connection. It is read-only and needs no Channel UUID.
{% endhint %}
