# Opt Out

## What is Opt Out?
Marks the contact as opted out of messaging when this Action runs.

## When does it trigger?
- When the flow reaches this `Opt Out` action while the flow is active and the channel is connected.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
### Open the flow and edit the Action node
In `Automations` > `Message Flows`, open a flow, select the `Action` step, and choose `Opt Out`.

📸 Screenshot placeholder:
> [Screenshot: Action step showing the Opt Out option]

{% endstep %}

{% endstepper %}

## What happens after it triggers?
The contact’s opt-out status is set, preventing further messaging until they opt in again; the flow continues along the path you set.

{% hint style="warning" %}
**Important behavior to know**

- **Permanent Action**: Once a contact opts out, they will not receive any future broadcasts or automated messages from your Message Flows. This is a compliance requirement for WhatsApp messaging.
- **Manual Re-opt-in Required**: Contacts who have opted out must manually opt back in before they can receive messages again. You cannot automatically re-add them to your messaging list.
- **Broadcast Exclusion**: Opted-out contacts are automatically excluded from all broadcasts, regardless of your selection criteria.
- **Compliance**: This action helps you comply with WhatsApp's messaging policies and regulations regarding user consent.
- **Use Confirmation Message**: Always use this action alongside a confirmation message so users know they've been unsubscribed.
{% endhint %}

## Common issues & solutions
- Contact still receives messages: confirm downstream flows respect opt-out and that opt-out runs on the published path.

## Best practice 💡
- Provide a clear confirmation and a way to re-opt in if appropriate.
- Keep opt-out paths simple to avoid accidental sends afterward.
