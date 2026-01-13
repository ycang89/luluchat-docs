# Flows

## What is the Flows tab?
The Flows tab lets you view which Message Flow the contact is currently in and manually trigger a Message Flow for the contact directly from contact info while in Inbox.

## When does it trigger?
- When you pick and send a Message Flow from the `Flows` tab in contact info.

## How to use (Step by Step)

{% stepper %}
{% step %}
### Open contact info

In `Inbox`, open the conversation and select the `Flows` tab.

📸 Screenshot placeholder:
> [Screenshot: Flows tab showing current flow status]
{% endstep %}

{% step %}
### View current flow (if active)

If the contact is currently in a Message Flow, you'll see the active flow name and status displayed at the top of the Flows tab. This helps you understand what automation is currently running for this contact.

📸 Screenshot placeholder:
> [Screenshot: Current flow indicator showing active flow name]
{% endstep %}

{% step %}
### Choose a flow and send

Select a published Message Flow from the dropdown and click Send to manually trigger it for the contact.

📸 Screenshot placeholder:
> [Screenshot: Flow selection dropdown and Send button]
{% endstep %}
{% endstepper %}

## What happens after it triggers?
The selected flow runs immediately for the contact, sending its configured steps.

## Important behavior to know
- **Current Flow Display**: The Flows tab shows which Message Flow the contact is currently in, if any.
- Only published flows appear in the dropdown; respect opt-out status before sending.
- Channel connectivity is required.

## Common issues & solutions
- Flow not listed: ensure it’s published and you have channel access.
- No response: verify channel connection and that the flow has active steps.

## Best practice 💡
- Use concise, goal-focused flows for manual sends.
