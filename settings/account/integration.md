# Settings: Integration

## What is Integration?
Connect Luluchat with external platforms and manage API access tokens for custom integrations.

## When does it trigger?
- When you need to connect Luluchat with external services like Zapier, Shopify, ChatGPT, or other apps.
- When you want to generate API access tokens for custom integrations or direct API access.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
### Access Integration Settings

Go to `Settings` from the left menu, then select `Account Management` > `Integration`.

📸 Screenshot placeholder:
> [Screenshot: Settings page with Integration tab selected]
{% endstep %}

{% step %}
### Manage External API Keys

In the Integration settings page, you'll see:

- **Zapier API Key**: A copyable API key that you can use to connect Luluchat with your Zapier workflows. Click the copy icon to copy the key.
- **WABA Permanent Access Token** (if you have WhatsApp Cloud API access): Enter your permanent token here to maintain connectivity with WhatsApp Business API.

📸 Screenshot placeholder:
> [Screenshot: Integration page showing Zapier API Key and WABA token fields]
{% endstep %}

{% step %}
### Browse and Connect Apps

Scroll to the **Apps** section to see all available native integrations (e.g., Shopify, ChatGPT, CRM systems). Click on any app card to view details and configure specific settings for that integration.

📸 Screenshot placeholder:
> [Screenshot: Available Apps grid showing integration cards]
{% endstep %}

{% step %}
### Manage Access Tokens

In the **Access Token** section, you can:
- View all existing access tokens used for direct Luluchat API requests
- Create new access tokens for API authentication
- Revoke tokens that are no longer in use

📸 Screenshot placeholder:
> [Screenshot: Access Token management table with create and revoke options]
{% endstep %}
{% endstepper %}

## What happens after it triggers?
- **API Keys Available**: Your Zapier API key is ready to use in Zapier workflows.
- **Apps Connected**: Native integrations become available for configuration.
- **Tokens Generated**: New access tokens can be used to authenticate API requests to Luluchat.

## Important behavior to know
- **Token Security**: Treat API keys and access tokens like passwords. Never share them publicly or commit them to code repositories.
- **Authorization**: Most API requests require a `Bearer` token in the Authorization header.
- **WABA Token**: The WABA Permanent Access Token is only visible if you have WhatsApp Cloud API (WABA) access enabled.
- **Token Revocation**: Revoking an access token immediately invalidates it. Any systems using that token will need to be updated with a new token.

## Common issues & solutions
- **Zapier connection not working**: Verify you're using the correct Zapier API Key from this page. Make sure you copied the entire key without any extra spaces.
- **Token not working**: Check that you're using the token in the correct format (Bearer token in Authorization header). Ensure the token hasn't been revoked.
- **Can't see WABA token field**: This field only appears if your account has WhatsApp Cloud API (WABA) access. Contact support if you believe you should have access.

## Best practice 💡
- **Revoke Unused Tokens**: Periodically audit your Access Token table and delete any tokens that are no longer in use to maintain security.
- **Specific Permissions**: Only generate tokens for the specific environments or use cases that need them.
- **Secure Storage**: Store API keys and tokens securely. Consider using environment variables or secure vaults for production applications.
- **Regular Rotation**: Consider rotating access tokens periodically for enhanced security.

## Related Documentation
- [Zapier Integration](./zapier-integration.md) - Learn how to set up Zapier workflows with Luluchat
- [Shopify Integration](./shopify-integration.md) - Learn how to connect your Shopify store
- [ChatGPT Integration](./chatgpt-integration.md) - Learn how to connect ChatGPT for AI features
- [WhatsApp Business App (WABA)](../whatsapp-business-app-waba/index.md) - Learn about WABA features and configuration
