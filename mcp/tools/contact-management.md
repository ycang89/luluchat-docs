# Contact Management

Tools for reading and updating contacts: conversations, internal notes, tags, assignee, collaborators, subscription status and custom attributes.

{% hint style="info" %}
`channel_uuid` and `contact_number` are explained in [Common parameters](index.md#common-parameters).
{% endhint %}

## Conversations & Notes

### get\_chat\_messages

**Read** · Read the actual WhatsApp messages exchanged with a contact. Returns the most recent page of the conversation, ordered oldest-first so it reads like a transcript.

**Example prompt:** *"What did +60123456789 say about the refund?"*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number, or a group ID ending in `@g.us` |
| `limit` | No | Messages per page, 1–100 (default 30) |
| `before_id` | No | Get messages older than this message ID (to page back through history) |
| `after_id` | No | Get messages newer than this message ID |
| `from` / `to` | No | Only messages between these dates (`YYYY-MM-DD`, team timezone) |
| `sent_by` | No | `contact`, `team` or `all` (default) |
| `search` | No | Text search, 2–100 characters |

{% hint style="warning" %}
`search` only covers the **last 4 months** and returns at most about 100 of the newest matches. To read older history, page back with `before_id`. Internal notes are **not** included. Use `get_contact_notes` for those.
{% endhint %}

### get\_contact\_notes

**Read** · Read the internal, staff-only notes on a contact. Pinned notes come first, then newest first.

**Example prompt:** *"What internal notes do we have on +60123456789?"*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `page` / `per_page` | No | Pagination (default 15 per page, max 100) |

### add\_note\_to\_contact

**Write** · Add an internal note to a contact. The note is **never sent to the customer**. It appears in the Inbox for your team, with the author **AI Agent (Tools)**.

**Example prompt:** *"Leave a note on +60123456789: customer wants delivery after 6pm."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `message` | Yes | Note text, plain text up to 1000 characters |

## Contact Details

### get\_contact

**Read** · Get full contact details: name, number, email, tags, custom attributes, assignee and collaborators. Assistants usually call this before changing a contact.

**Example prompt:** *"Show me the details for +60123456789."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number with country code |

### update\_contact\_subscription

**Write** · Opt a contact in or out of automated messages.

**Example prompt:** *"Unsubscribe +60123456789 from automated messages."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `is_subscribed` | Yes | `true` to opt in, `false` to opt out |

{% hint style="danger" %}
**Opting out immediately stops all running message flows for the contact and cannot be undone.** Opting back in only allows *new* automations to start. Stopped flows are not resumed. Your team can still send manual messages to opted-out contacts.
{% endhint %}

## Tags

### get\_tags

**Read** · List all tags in your team. Useful to check the exact spelling before tagging (tag names are case-sensitive).

**Example prompt:** *"Show me all tags that contain VIP."*

| Parameter | Required | Description |
| --- | --- | --- |
| `name` | No | Search by tag name (partial match) |
| `sort` | No | `name` (default), `created_at` or `priority` |
| `order` | No | `asc` (default) or `desc` |
| `page` / `per_page` | No | Pagination (default 50 per page, max 200) |

### add\_tag\_to\_contact

**Write** · Add a tag to a contact. If the tag doesn't exist yet, it is created. Adding a tag can trigger your [Workflows](../../automations/workflows.md).

**Example prompt:** *"Tag +60123456789 as VIP Customer in red."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `tag_name` | Yes | Tag name (case-sensitive) |
| `tag_color` | No | Hex color for a **new** tag, e.g. `#FF5733` (default blue `#2A8ADE`) |

### remove\_tag\_from\_contact

**Write** · Remove a tag from a contact. The tag itself stays in your workspace.

**Example prompt:** *"Remove the Hot Lead tag from +60123456789."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `tag_name` | Yes | Exact tag name (case-sensitive) |

## Assignee & Collaborators

### assign\_assignee\_to\_contact

**Write** · Set the team member who owns the contact, or remove the assignee. A contact has only one assignee.

**Example prompt:** *"Assign +60123456789 to Alvan."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `staff_id` | Yes | Team member ID from [`get_team_staff`](workspace-management.md#get_team_staff). Use `0` to remove the assignee |

### add\_collaborator\_to\_contact

**Write** · Add a team member as a collaborator. A contact can have many collaborators.

**Example prompt:** *"Add Sarah as a collaborator on +60123456789."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `staff_id` | Yes | Team member ID from [`get_team_staff`](workspace-management.md#get_team_staff) |

### remove\_collaborator\_from\_contact

**Write** · Remove a collaborator from a contact.

**Example prompt:** *"Remove Sarah from the collaborators of +60123456789."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `staff_id` | Yes | Team member ID of the collaborator |

## Custom Attributes

### get\_attributes

**Read** · List all [custom attributes](../../settings/data/custom-attributes.md) defined in your team.

**Example prompt:** *"What custom attributes do we have?"*

| Parameter | Required | Description |
| --- | --- | --- |
| `sort_by` | No | `name` (default) or `created_at` |
| `sort_order` | No | `asc` (default) or `desc` |

### assign\_attribute\_to\_contact

**Write** · Set a custom attribute value on a contact. If the attribute doesn't exist yet, it is created with the given data type.

**Example prompt:** *"Set the birthday of +60123456789 to 25 December."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `attribute_name` | Yes | Attribute name, e.g. `customer_segment` (case-sensitive) |
| `value` | Yes | Value, max 255 characters. Format must match the data type |
| `data_type` | No | `string` (default), `numeric`, `date` (`YYYY-MM-DD`), `time` (`HH:MM:SS`) or `anniversal_date` (`MM-DD`) |

### remove\_attribute\_from\_contact

**Write** · Clear a custom attribute value from a contact. The attribute stays available for other contacts.

**Example prompt:** *"Remove the customer\_segment attribute from +60123456789."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `attribute_name` | Yes | Attribute name to clear |
