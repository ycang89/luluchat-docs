# Settings: Integration

## What is Integration?
Connect Luluchat with external platforms and manage API access tokens for custom integrations.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
### External API Keys

- Zapier API Key: Use this key to connect Luluchat with your Zapier workflows.
- WABA Permanent Access Token: If using WhatsApp Cloud API, enter your permanent token here to maintain connectivity.

📸 Screenshot placeholder:
> [Screenshot: Zapier and WABA token fields]
{% endstep %}

{% step %}
### Browse and Connect Apps

The Apps section lists all native integrations (e.g., Shopify, CRM). Click a card to configure specific settings for that app.

📸 Screenshot placeholder:
> [Screenshot: Available Apps grid]
{% endstep %}

{% step %}
### Manage Access Tokens

The Access Token table shows tokens used for direct Luluchat API requests. You can view, create, or revoke tokens here.

📸 Screenshot placeholder:
> [Screenshot: Access Token management table]
{% endstep %}
{% endstepper %}

## Important behavior to know
- **Token Security**: Treat API keys and access tokens like passwords. Never share them publicly.
- **Authorization**: Most API requests require a `Bearer` token header.

## Best practice 💡
- **Revoke Unused Tokens**: Periodically audit your Access Token table and delete any tokens that are no longer in use.
- **Specific Permissions**: Ensure you only generate tokens for the environments that need them.
