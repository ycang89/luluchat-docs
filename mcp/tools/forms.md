# Forms

Tools for sharing your [Forms](../../forms/index.md) with contacts.

{% hint style="info" %}
**Typical flow:** `get_forms` → `generate_form_link_for_contact`
{% endhint %}

### get\_forms

**Read** · List your team's forms with their IDs, status and public URLs.

**Example prompt:** *"Show me all active forms."*

| Parameter | Required | Description |
| --- | --- | --- |
| `name` | No | Search by form name or title |
| `status` | No | `active` or `inactive` (default all) |
| `sort` | No | `name` (default), `title`, `status`, `created_at` or `updated_at` |
| `order` | No | `asc` (default) or `desc` |
| `page` / `per_page` | No | Pagination (default 20 per page, max 100) |

### generate\_form\_link\_for\_contact

**Write** · Create a personalised form link for a contact. The link pre-fills the contact's details and links the response back to that contact. If the contact has an unfinished form, the same link is reused so they can continue.

**Example prompt:** *"Generate the registration form link for +60123456789."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `form_id` | Yes | Active form ID from `get_forms` |

{% hint style="success" %}
Use a personalised link instead of the form's public URL. Otherwise the response isn't linked to the contact.
{% endhint %}
