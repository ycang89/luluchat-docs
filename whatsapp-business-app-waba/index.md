# WhatsApp Business App (WABA)

## What is WABA?

WhatsApp Business App (WABA), also known as WhatsApp Cloud API, is the official business messaging platform provided by Meta. It allows businesses to communicate with customers at scale through WhatsApp with advanced features like message templates, verified business status, and detailed analytics.

Unlike WhatsApp Personal (which connects your personal WhatsApp account), WABA is designed specifically for businesses and provides enterprise-grade messaging capabilities.

## Key Concepts

To help you understand and effectively use WABA, we've broken down the essential concepts into separate guides:

{% cards %}
{% card title="Service Window" description="Learn about the 24-hour messaging window and how to maintain free conversations" icon="clock" %}
[Read More →](./service-window.md)
{% endcard %}

{% card title="Charging & Pricing" description="Understand conversation-based pricing and how WABA charges work" icon="dollar-sign" %}
[Read More →](./charging-pricing.md)
{% endcard %}

{% card title="Message Template Types" description="Explore the different template categories and when to use each" icon="file-text" %}
[Read More →](./message-template-types.md)
{% endcard %}

{% card title="Coexistence" description="Learn about using both Personal and WABA accounts together" icon="link" %}
[Read More →](./coexistence.md)
{% endcard %}

{% card title="Business Verification" description="Learn how business verification helps unlock higher messaging tiers" icon="shield-check" %}
[Read More →](./business-verification.md)
{% endcard %}

{% card title="Blue Tick (Verified Business)" description="Discover the benefits of business verification and how to get verified" icon="check-circle" %}
[Read More →](./blue-tick-verification.md)
{% endcard %}

{% card title="Messaging Limits & Quality" description="Understand account tiers, messaging limits, and quality rating system" icon="bar-chart" %}
[Read More →](./messaging-limits-quality.md)
{% endcard %}
{% endcards %}

## Important Behavior to Know

- **Policy Changes**: WhatsApp frequently updates policies, features, and pricing. Always refer to official documentation for the latest information.
- **Regional Differences**: Rules, pricing, and features may vary by country or region.
- **Approval Times**: Template approvals can take minutes to 24 hours, depending on category and content.
- **Quality Score**: Your messaging quality affects template approval and account standing. Maintain high-quality, relevant conversations.
- **Rate Limits**: WABA has rate limits on messaging. Exceeding limits can result in temporary restrictions.

## Official Documentation Reference

{% hint style="warning" %}
**Important**: WhatsApp Business API policies, features, and pricing change frequently. Always refer to the official Meta documentation for the most current and accurate information.
{% endhint %}

**Key Resources**:

- **[WhatsApp Business API Get Started](https://developers.facebook.com/documentation/business-messaging/whatsapp/get-started)**: Official getting started guide
- **[WhatsApp Business API Pricing](https://developers.facebook.com/docs/whatsapp/pricing)**: Current pricing information
- **[Message Templates Documentation](https://developers.facebook.com/docs/whatsapp/business-platform/guides/send-messages)**: Template guidelines and requirements
- **[Business Verification](https://www.facebook.com/business/help/2058515294227817)**: How to get verified
- **[WhatsApp Business Policy](https://www.whatsapp.com/legal/business-policy)**: Official business policies

## Related Documentation

- [Message Templates](../message-templates.md) - Learn how to create and manage message templates in Luluchat
- [Connect Your Channel](../inbox/connect-channel.md) - Learn how to connect your WABA account
- [Integration Settings](../settings/account/integration.md) - Manage your WABA Permanent Access Token
- [Broadcasts](../broadcasts.md) - Learn how to send messages to multiple customers using templates
