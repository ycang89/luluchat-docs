# Ticketing

Tools for managing support tickets (see [Tickets](../../tickets/index.md)).

{% hint style="info" %}
**Typical flow:** `get_ticket_pipelines` → `get_stages` → `create_ticket` / `update_ticket`
{% endhint %}

## Pipelines & Stages

### get\_ticket\_pipelines

**Read** · List your ticket pipelines and their UUIDs.

**Example prompt:** *"Show me all ticket pipelines."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `include_archived` | No | Include archived pipelines (default `false`) |

### get\_stages

**Read** · List the stages in a ticket pipeline, including which stages are **Done**.

**Example prompt:** *"What stages are in the Support Pipeline?"*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `pipeline_uuid` | Yes | Pipeline UUID from `get_ticket_pipelines` |
| `include_archived` | No | Include archived stages (default `false`) |

## Tickets

### create\_ticket

**Write** · Create a new ticket for a contact. If no pipeline or stage is given, the first active pipeline and its first open stage are used.

**Example prompt:** *"Create a ticket 'Payment failed' for +60123456789."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `title` | Yes | Ticket title, max 255 characters |
| `pipeline_uuid` | No | Pipeline UUID from `get_ticket_pipelines` |
| `stage_uuid` | No | Stage UUID from `get_stages` |
| `description` | No | Up to 5000 characters |
| `collaborators` | No | List of team member UUIDs |
| `attachments` | No | List of `{ "title": "...", "url": "https://..." }` |

### get\_ticket

**Read** · Get the full details of one ticket: stage, contact, assignment, comment count and attachments.

**Example prompt:** *"Show me the details of the Payment failed ticket."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `ticket_uuid` | Yes | Ticket UUID from `get_contact_tickets` or `create_ticket` |

### get\_contact\_tickets

**Read** · List all tickets linked to a contact.

**Example prompt:** *"Does +60123456789 have any open tickets?"*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `page` / `per_page` | No | Pagination (default 15 per page, max 100) |

### update\_ticket

**Write** · Update one or more fields of a ticket, or move it to another stage. Fields you don't include stay the same.

**Example prompt:** *"Move the Payment failed ticket to In Progress."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `ticket_uuid` | Yes | Ticket UUID |
| `title` | No | New title |
| `description` | No | New description |
| `stage_uuid` | No | Move to another stage in the **same** pipeline |
| `contact_number` | No | Link the ticket to a different contact |
| `position` | No | Position within the stage (`0` = top) |

## Comments

### get\_ticket\_comments

**Read** · Read the comments on a ticket, with authors, attachments and timestamps.

**Example prompt:** *"Show me the comments on the Payment failed ticket."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `ticket_uuid` | Yes | Ticket UUID |
| `page` / `per_page` | No | Pagination (default 15 per page, max 100) |

### add\_ticket\_comment

**Write** · Add a comment to a ticket, with optional attachments.

**Example prompt:** *"Comment on the Payment failed ticket: customer confirmed the issue is resolved."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `ticket_uuid` | Yes | Ticket UUID |
| `message` | Yes | Comment text, max **255** characters |
| `attachments` | No | List of `{ "title": "...", "url": "https://..." }`. URLs must be publicly accessible |
