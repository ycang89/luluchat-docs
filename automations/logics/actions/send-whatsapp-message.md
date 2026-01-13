# Send WhatsApp Message

## What is Send WhatsApp Message?

Sends a manual WhatsApp message to a specific number from a flow step (available where direct sending is allowed).

## When does it trigger?

* When the flow reaches this `Send WhatsApp Message` action while the flow is active and the channel is connected.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Open the flow and edit the Action node

In `Automations` > `Message Flows`, open a flow, select the `Action` step, and choose `Send WhatsApp Message`.

📸 Screenshot placeholder:

> \[Screenshot: Action step showing the Send WhatsApp Message option]
{% endstep %}
{% endstepper %}

## What happens after it triggers?

The message is sent to the specified number; the flow continues to the next step.

## Important behavior to know

* Use valid international format numbers.
* Sending depends on channel connectivity and any provider limits.

## Common issues & solutions

* Message not delivered: confirm the number format and that the channel is connected.
* Option unavailable: this action may be hidden for certain channel types or permissions.

## Best practice 💡

* Keep these messages concise and clearly branded.
* Avoid overuse to prevent rate limits; use templates where compliance is required.
