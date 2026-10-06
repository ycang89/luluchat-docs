# Available Tools

The Luluchat MCP Server provides the tools below. They are grouped the same way as the **MCP Tool Permissions** list in `Settings > Tools > AI`, so you can quickly find a tool and turn it on or off.

{% hint style="info" %}
You don't need to call these tools yourself. Just ask your AI assistant in plain language, e.g. *"Create a support ticket for +60123456789 about a failed payment"*, and it picks the right tools.
{% endhint %}

## Tool groups

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Contact Management</strong></td><td>Contacts, chat messages, notes, tags, assignee, collaborators, subscription and custom attributes</td><td><a href="contact-management.md">contact-management.md</a></td></tr><tr><td><strong>Inbox Tabs</strong></td><td>List inbox tabs and add or remove contacts from custom tabs</td><td><a href="inbox-tabs.md">inbox-tabs.md</a></td></tr><tr><td><strong>Workspace Management</strong></td><td>List your channels and team members</td><td><a href="workspace-management.md">workspace-management.md</a></td></tr><tr><td><strong>Deal</strong></td><td>Pipelines, stages and deal cards</td><td><a href="deal.md">deal.md</a></td></tr><tr><td><strong>Ticketing</strong></td><td>Pipelines, stages, tickets and ticket comments</td><td><a href="ticketing.md">ticketing.md</a></td></tr><tr><td><strong>Forms</strong></td><td>List forms and create personalised form links</td><td><a href="forms.md">forms.md</a></td></tr><tr><td><strong>Booking</strong></td><td>Calendars and appointments</td><td><a href="booking.md">booking.md</a></td></tr></tbody></table>

## All tools at a glance

**Type** shows whether a tool only reads data (**Read**) or makes changes (**Write**).

### Contact Management

| Tool | Type | What it does |
| --- | --- | --- |
| [`get_chat_messages`](contact-management.md#get_chat_messages) | Read | Read WhatsApp messages exchanged with a contact |
| [`get_contact`](contact-management.md#get_contact) | Read | Get a contact's details, tags, attributes, assignee and collaborators |
| [`add_note_to_contact`](contact-management.md#add_note_to_contact) | Write | Add an internal, staff-only note |
| [`get_contact_notes`](contact-management.md#get_contact_notes) | Read | Read a contact's internal notes |
| [`get_tags`](contact-management.md#get_tags) | Read | List all tags in your team |
| [`add_tag_to_contact`](contact-management.md#add_tag_to_contact) | Write | Add a tag (creates it if it doesn't exist) |
| [`remove_tag_from_contact`](contact-management.md#remove_tag_from_contact) | Write | Remove a tag from a contact |
| [`assign_assignee_to_contact`](contact-management.md#assign_assignee_to_contact) | Write | Set or remove the contact's assignee |
| [`add_collaborator_to_contact`](contact-management.md#add_collaborator_to_contact) | Write | Add a team member as collaborator |
| [`remove_collaborator_from_contact`](contact-management.md#remove_collaborator_from_contact) | Write | Remove a collaborator |
| [`update_contact_subscription`](contact-management.md#update_contact_subscription) | Write | Opt a contact in or out of automated messages |
| [`get_attributes`](contact-management.md#get_attributes) | Read | List all custom attributes |
| [`assign_attribute_to_contact`](contact-management.md#assign_attribute_to_contact) | Write | Set a custom attribute value |
| [`remove_attribute_from_contact`](contact-management.md#remove_attribute_from_contact) | Write | Clear a custom attribute value |

### Inbox Tabs

| Tool | Type | What it does |
| --- | --- | --- |
| [`get_inbox_tabs`](inbox-tabs.md#get_inbox_tabs) | Read | List inbox tabs |
| [`assign_contact_to_inbox_tab`](inbox-tabs.md#assign_contact_to_inbox_tab) | Write | Add a contact to a custom tab |
| [`remove_contact_from_inbox_tab`](inbox-tabs.md#remove_contact_from_inbox_tab) | Write | Remove a contact from a tab |

### Workspace Management

| Tool | Type | What it does |
| --- | --- | --- |
| [`get_channels`](workspace-management.md#get_channels) | Read | List channels and their UUIDs |
| [`get_team_staff`](workspace-management.md#get_team_staff) | Read | List team members and their IDs |

### Deal

| Tool | Type | What it does |
| --- | --- | --- |
| [`get_deal_pipelines`](deal.md#get_deal_pipelines) | Read | List deal pipelines |
| [`get_deal_stages`](deal.md#get_deal_stages) | Read | List stages in a deal pipeline |
| [`create_deal`](deal.md#create_deal) | Write | Create a deal for a contact |
| [`get_deal`](deal.md#get_deal) | Read | Get a deal's details |
| [`update_deal`](deal.md#update_deal) | Write | Update a deal's fields |
| [`get_contact_deals`](deal.md#get_contact_deals) | Read | List all deals of a contact |
| [`move_deal_to_stage`](deal.md#move_deal_to_stage) | Write | Move a deal to another stage |

### Ticketing

| Tool | Type | What it does |
| --- | --- | --- |
| [`get_ticket_pipelines`](ticketing.md#get_ticket_pipelines) | Read | List ticket pipelines |
| [`get_stages`](ticketing.md#get_stages) | Read | List stages in a ticket pipeline |
| [`create_ticket`](ticketing.md#create_ticket) | Write | Create a ticket for a contact |
| [`get_ticket`](ticketing.md#get_ticket) | Read | Get a ticket's details |
| [`update_ticket`](ticketing.md#update_ticket) | Write | Update a ticket or move it to another stage |
| [`get_contact_tickets`](ticketing.md#get_contact_tickets) | Read | List all tickets of a contact |
| [`get_ticket_comments`](ticketing.md#get_ticket_comments) | Read | Read a ticket's comments |
| [`add_ticket_comment`](ticketing.md#add_ticket_comment) | Write | Add a comment to a ticket |

### Forms

| Tool | Type | What it does |
| --- | --- | --- |
| [`get_forms`](forms.md#get_forms) | Read | List forms |
| [`generate_form_link_for_contact`](forms.md#generate_form_link_for_contact) | Write | Create a personalised form link for a contact |

### Booking

| Tool | Type | What it does |
| --- | --- | --- |
| [`get_booking_calendars`](booking.md#get_booking_calendars) | Read | List booking calendars |
| [`get_booking_appointment`](booking.md#get_booking_appointment) | Read | Get one appointment's details |
| [`get_contact_booking_appointments`](booking.md#get_contact_booking_appointments) | Read | List a contact's appointments |

## Common parameters

Most tools share these parameters:

| Parameter | What it is | Where to find it |
| --- | --- | --- |
| `channel_uuid` | The WhatsApp channel to work with, e.g. `550e8400-e29b-41d4-a716-446655440000` | Click **Channels** in the header bar and copy the **ID** on the channel card, or let the assistant look it up with [`get_channels`](workspace-management.md#get_channels) |
| `contact_number` | The contact's WhatsApp number with country code, e.g. `+60123456789` | The contact's profile in the Inbox |

IDs such as `staff_id`, `tab_id`, `pipeline_uuid`, `stage_uuid`, `deal_uuid`, `ticket_uuid` and `form_id` are looked up by the assistant using the matching `get_...` tool, so you can refer to things by name, e.g. *"assign to Sarah"* or *"move to the Qualified stage"*.

## Important behavior to know

* **Turned-off tools are hidden**: Only tools turned on in `Settings > Tools > AI` can be used.
* **Safe to retry**: Most add/remove tools are idempotent. Running them twice doesn't create duplicates or errors.
* **Team scoped**: Every tool only works with data from the team that owns the access token.
