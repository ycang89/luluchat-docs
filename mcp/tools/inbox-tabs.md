# Inbox Tabs

Tools for organising contacts into inbox tabs (see [Custom Lists](../../inbox/custom-lists.md)).

{% hint style="info" %}
Only **custom tabs** can have contacts added manually. System tabs such as *All* or *Unread* are filled automatically.
{% endhint %}

### get\_inbox\_tabs

**Read** · List the inbox tabs in your team, including their IDs and whether they are custom tabs.

**Example prompt:** *"Show me all my custom inbox tabs."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `type` | No | `custom` for your own tabs, `default` for system tabs, or leave empty for all |
| `include_hidden` | No | Include tabs hidden in the Inbox (default `true`) |

### assign\_contact\_to\_inbox\_tab

**Write** · Add a contact to a custom inbox tab.

**Example prompt:** *"Add +60123456789 to the VIP Customers tab."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `tab_id` | Yes | Custom tab ID from `get_inbox_tabs` |

### remove\_contact\_from\_inbox\_tab

**Write** · Remove a contact from an inbox tab.

**Example prompt:** *"Remove +60123456789 from the VIP Customers tab."*

| Parameter | Required | Description |
| --- | --- | --- |
| `channel_uuid` | Yes | Channel UUID |
| `contact_number` | Yes | Contact number |
| `tab_id` | Yes | Tab ID from `get_inbox_tabs` |
