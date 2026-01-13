# Message Flows

## What is Message Flows Settings?

Manage global behavior for automated conversations, including typing indicators and webhook security.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Enable Typing Indicators

Make your bot feel more human by showing a "typing..." status before automated messages are sent.

* WhatsApp Personal: Enable for standard WhatsApp accounts.
* WhatsApp Cloud: Enable for official Business API accounts.
* Effect: When enabled, the system respects the "Typing Wait Time" configured in your individual Message Flow nodes.

📸 Screenshot placeholder:

> \[Screenshot: Typing Indicator switches for Personal and Cloud]
{% endstep %}

{% step %}
#### Configure Webhook Security

If your Message Flows call external URLs, use these settings to secure the connection.

* Enable Webhook Authorization: Toggle "On" to require an authorization key for any outgoing webhook requests.
* Webhook Authorization Key: Click `Reset` to generate a new key. Copy the `Bearer` token to use in your external system's security headers.

📸 Screenshot placeholder:

> \[Screenshot: Webhook security section with Authorization Key and Reset button]
{% endstep %}
{% endstepper %}

## Important behavior to know

* **Typing Wait Time**: Typing indicators only show if the specific Message Node in your flow has a delay value set.
* **Webhook Impact**: Resetting your Authorization Key will break existing integrations until you update your external systems with the new key.

## Best practice 💡

* **Realistic Delays**: Set typing wait times to match the length of the message (e.g., 2-3 seconds) for a natural feel.
* **Secure Webhooks**: Always enable Webhook Authorization when sending sensitive contact data to external servers.
