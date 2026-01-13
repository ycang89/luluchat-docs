# Delay

## What is Delay?

Pauses the flow for a set duration before moving to the next step.

## When does it trigger?

* When the flow reaches this `Delay` action while the flow is active and the channel is connected.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Open the flow and edit the Action node

In `Automations` > `Message Flows`, open a flow, select the `Action` step, and choose `Delay`.

📸 Screenshot placeholder:

> \[Screenshot: Action step showing the Delay option]
{% endstep %}
{% endstepper %}

## What happens after it triggers?

The flow pauses for the duration you set, then continues to the next connected step.

## Important behavior to know

* Delay is fixed time; it does not check for replies.
* Long delays postpone all downstream actions until the timer completes.

## Common issues & solutions

* Step never continues: confirm the delay duration isn’t excessively long and the flow path remains published.

## Best practice 💡

* Keep delays short for responsiveness; use `Smart Delay` or `Wait for Reply` when you need branching.
