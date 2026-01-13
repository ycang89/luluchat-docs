# Default Flow

## What is Default Flow?

The catch-all message flow that runs when no other specific trigger (keyword, growth tool, widget, workflow) matches. It ensures every inbound contact gets a basic response and path forward.

## When does it trigger?

* When a contact messages your channel and no keyword/growth-tool/widget/workflow trigger applies.
* Only if a Default Flow is configured and the channel is connected.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Open Message Flows

Go to `Automations` → `Message Flows` and choose to create or edit the Default Flow.

📸 Screenshot placeholder:

> \[Screenshot: Message Flows list showing Default Flow option]
{% endstep %}

{% step %}
#### Build the Default Flow

Design the flow with a welcome message and key next steps (e.g., menu, handoff, intake questions). Save/publish.

📸 Screenshot placeholder:

> \[Screenshot: Default Flow builder with welcome and routing steps]
{% endstep %}

{% step %}
#### Enable as default

Ensure this flow is marked/assigned as the default for the channel.

📸 Screenshot placeholder:

> \[Screenshot: Setting indicating this flow is set as Default]
{% endstep %}
{% endstepper %}

## What happens after it triggers?

New inbound messages enter this flow and receive the configured steps, providing a response even without other triggers.

## Important behavior to know

* Default Flow is the fallback; more specific triggers take precedence.
* Channel must be connected; drafts won’t run.

## Common issues & solutions

* Default not firing: confirm it’s set as default and the channel is connected.
* Overridden by other triggers: check keywords/growth tools that may be matching instead.

## Best practice 💡

* Keep the default concise with clear next actions (menu or quick handoff).
* Include a fail-safe handoff to an agent or a catch-all inbox path.
