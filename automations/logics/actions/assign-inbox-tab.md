# Inbox List Assignment

## What is Inbox List Assignment?
Moves the conversation to a chosen inbox list/tab when this Action runs.

## When does it trigger?
- When the flow reaches this `Inbox List Assignment` action while the flow is active and the channel is connected.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
### Open the flow and edit the Action node
In `Automations` > `Message Flows`, open a flow, select the `Action` step, and choose `Inbox List Assignment`.

📸 Screenshot placeholder:
> [Screenshot: Action step showing the Inbox List Assignment option]

{% endstep %}

{% endstepper %}

## What happens after it triggers?
The conversation moves to the selected inbox list/tab; agents see it under that filter, and the flow continues.

## Important behavior to know
- Available lists depend on your inbox configuration and permissions.
- Moving lists does not change tags or assignees; combine with other actions if needed.

## Common issues & solutions
- List not available: confirm you have access or that the list exists.
- Conversation not moved: ensure the action is on a published path and the channel is connected.

## Best practice 💡
- Use lists to triage (e.g., VIP, Billing, Support) and pair with tags for clarity.
