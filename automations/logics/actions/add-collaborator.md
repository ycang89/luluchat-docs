# Add Collaborator

## What is Add Collaborator?
Adds selected teammates as collaborators on the conversation when this Action runs.

## When does it trigger?
- When the flow reaches this `Add Collaborator` action while the flow is active and the channel is connected.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
### Open the flow and edit the Action node
In `Automations` > `Message Flows`, open a flow, select the `Action` step, and choose `Add Collaborator`.

📸 Screenshot placeholder:
> [Screenshot: Action step showing the Add Collaborator option]

{% endstep %}

{% endstepper %}

## What happens after it triggers?
The chosen collaborators are added to the conversation so they can follow and respond; the flow continues.

## Important behavior to know
- Collaborators do not replace assignees; they are additional followers.
- Visibility depends on workspace permissions.

## Common issues & solutions
- Collaborator not added: confirm the action is on a published path and the user has access.
- User not listed: check the teammate’s permissions for this channel.

## Best practice 💡
- Add collaborators for specialists (e.g., billing, technical) without changing the main assignee.

