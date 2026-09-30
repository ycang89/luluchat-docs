# Add to Ticket Stage

## What is Add to Ticket Stage?

Creates a new ticket for the contact in the ticket pipeline and stage you choose, whenever a message flow reaches this action. Use it to turn customer requests into tickets automatically, e.g. when a customer picks *Report a problem* in a menu.

## When does it trigger?

* When the flow reaches this `Add to Ticket Stage` action while the flow is active.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Add the action

In `Automations` > `Message Flows`, open a flow, select an `Action` step, and choose **Add to Ticket Stage**.
{% endstep %}

{% step %}
#### Fill in the ticket details

| Field | Description |
| --- | --- |
| **Ticket Pipeline** | The pipeline to create the ticket in (required) |
| **Stage** | The stage the new ticket starts in (required) |
| **Title** | The ticket summary. You can use contact placeholders, e.g. `Issue from {{Display Name}}` |
| **Description** | Extra details, e.g. `Reported via WhatsApp: {{Push Name}}` |
| **Collaborators** | Team members to add to the ticket (optional) |
| **Insert a note into the conversation when ticket created** | Adds an internal note to the chat with the ticket number and a link to the ticket |

📸 Screenshot placeholder:

> \[Screenshot: Add to Ticket Stage action settings]
{% endstep %}

{% step %}
#### Save and publish the flow

Save the action and publish the flow.
{% endstep %}
{% endstepper %}

## What happens after it triggers?

* A new ticket is created and linked to the contact, with **Medium** priority.
* Placeholders in the Title and Description are replaced with the contact's details.
* If **Insert a note** is on, your team sees an internal note in the conversation, e.g. `🎫 Ticket created: [SUP-12] https://...`. The customer doesn't see this note.
* The flow continues to the next step.

## Important behavior to know

* **Creates a new ticket every time**: If the same contact goes through the action twice, they get two tickets. It doesn't move an existing ticket.
* Only available if your plan includes Tickets and you have access to it.
* The pipeline and stage must exist before you can select them.

## Common issues & solutions

* **No ticket created**: Check that the flow is published and the action is on the path the contact actually took.
* **Duplicate tickets**: Place the action where contacts only reach it once, or check for an open ticket in the conversation first.
* **Pipeline or stage missing**: Create it on the Tickets [Board](../../../tickets/board.md), then return to the flow.

## Best practice 💡

* Use a clear Title with placeholders so tickets are easy to recognise on the board.
* Turn on **Insert a note** so agents in the Inbox can see and open the ticket straight from the chat.
* Add collaborators so the right team is notified right away.
