# Opt-In Flow

## What is Opt-In Flow?
Captures a contact’s consent and updates their opt-in status, usually after they agree to receive messages.

## When does it trigger?
- When the flow is invoked on an opt-in path (e.g., via a trigger or manual run) to register consent.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
### Open Message Flows

Go to `Automations` → `Message Flows` and create/select the Opt-In Flow.

📸 Screenshot placeholder:
> [Screenshot: Message Flows list showing Opt-In Flow]
{% endstep %}

{% step %}
### Collect consent

Prompt the contact to agree (e.g., "Reply YES to continue"). Include clear consent language. Save/publish.

📸 Screenshot placeholder:
> [Screenshot: Opt-In Flow builder with consent prompt]
{% endstep %}

{% step %}
### Update status

Ensure the flow includes the opt-in action/update so the contact is marked as opted in.

📸 Screenshot placeholder:
> [Screenshot: Action step marking opt-in]
{% endstep %}
{% endstepper %}

## What happens after it triggers?
Consent is captured; the contact is marked opted in, and the flow can continue to the next steps (welcome, routing).

## Important behavior to know
- Use clear consent text; store proof where applicable.
- Opt-in status allows future messaging; opt-out overrides it.

## Common issues & solutions
- Status not updated: ensure the opt-in action runs and the flow is published.
- Trigger not firing: verify the opt-in path/trigger is set correctly.

## Best practice 💡
- Keep the opt-in ask simple and explicit.
- Confirm success with a short welcome message.
