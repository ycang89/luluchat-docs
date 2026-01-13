# Save to Attribute

## What is Save to Attribute?
Stores captured values into selected contact attributes when this Action runs.

## When does it trigger?
- When the flow reaches this `Save to Attribute` action while the flow is active and the channel is connected.
- It uses the latest mapped values from the flow context (e.g., form or prior reply).

## How to set it up (Step by Step)

{% stepper %}
{% step %}
### Open the flow and edit the Action node
In `Automations` > `Message Flows`, open a flow, select the `Action` step, and choose `Save to Attribute`.

📸 Screenshot placeholder:
> [Screenshot: Action step showing the Save to Attribute option]

{% endstep %}

{% endstepper %}

## What happens after it triggers?
The chosen attributes on the contact record are updated with the mapped values; the flow continues to the next step.

## Important behavior to know
- Only attributes you select are updated; others stay unchanged.
- Ensure the needed data exists earlier in the flow (form answers, replies, or variables).

## Common issues & solutions
- Attribute remains blank: confirm the source data is available and the action is on a published path.
- Attribute not listed: create it in Data Management or check permissions.

## Best practice 💡
- Map attributes immediately after collecting data to avoid missing context.
- Use clear attribute names and keep consistent formatting (e.g., title case vs lowercase).
