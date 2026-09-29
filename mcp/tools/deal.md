# Deal

Tools for managing your sales pipeline (see [Deals](../../deals/index.md)).

{% hint style="info" %}
**Typical flow:** `get_deal_pipelines` → `get_deal_stages` → `create_deal` / `move_deal_to_stage`
{% endhint %}

## Pipelines & Stages

### get\_deal\_pipelines

**Read** · List your deal pipelines and their UUIDs.

**Example prompt:** *"Show me all deal pipelines."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `include_archived` | No | Include archived pipelines (default `false`) |
| `page` / `per_page` | No | Pagination (default 15 per page, max 100) |

### get\_deal\_stages

**Read** · List the stages in a deal pipeline, including which stages are **Won** and **Lost**.

**Example prompt:** *"What stages are in the Sales Pipeline?"*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `pipeline_uuid` | Yes | Pipeline UUID from `get_deal_pipelines` |
| `include_archived` | No | Include archived stages (default `false`) |

## Deals

### create\_deal

**Write** · Create a new deal for a contact.

**Example prompt:** *"Create a deal 'Enterprise License' worth 50,000 for +60123456789 in the Sales Pipeline, due 31 Dec."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `title` | Yes | Deal title, max 255 characters |
| `pipeline_uuid` | Yes | Pipeline UUID from `get_deal_pipelines` |
| `stage_uuid` | No | Starting stage. If empty, the pipeline's default stage is used |
| `amount` | No | Deal value (currency follows your team settings) |
| `priority` | No | 1 (lowest) – 10 (highest), default 5 |
| `due_date` | No | Target close date, `YYYY-MM-DD` |
| `description` | No | Up to 1000 characters |
| `remarks` | No | Internal team remarks, up to 2000 characters |
| `collaborator_uuids` | No | List of team member UUIDs |
| `attachments` | No | List of `{ "title": "...", "url": "https://..." }` |

### get\_deal

**Read** · Get the full details of one deal: stage, contact, amount, collaborators, tags and attachments.

**Example prompt:** *"Show me the details of the Enterprise License deal."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `deal_uuid` | Yes | Deal UUID from `get_contact_deals` or `create_deal` |

### get\_contact\_deals

**Read** · List all deals linked to a contact.

**Example prompt:** *"What deals does +60123456789 have?"*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `page` / `per_page` | No | Pagination (default 15 per page, max 100) |

### update\_deal

**Write** · Update one or more fields of a deal. Fields you don't include stay the same. Send `null` to clear `amount`, `priority`, `due_date` or `remarks`.

**Example prompt:** *"Change the Enterprise License deal amount to 75,000 and priority to 9."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `deal_uuid` | Yes | Deal UUID |
| `title`, `amount`, `priority`, `due_date`, `description`, `remarks` | No | New values |
| `stage_uuid` | No | Move to another stage in the **same** pipeline |
| `contact_number` | No | Link the deal to a different contact |

### move\_deal\_to\_stage

**Write** · Move a deal to another stage in the same pipeline. Moving to a **Won** or **Lost** stage closes the deal.

**Example prompt:** *"Move the Enterprise License deal to Qualified."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `deal_uuid` | Yes | Deal UUID |
| `stage_uuid` | Yes | Target stage UUID from `get_deal_stages` |
