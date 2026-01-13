# Charging and Pricing

## How WABA charges work

WABA uses a **conversation-based pricing model**. A conversation is a 24-hour session that starts when you send a message to a customer (or when they message you).

## Conversation Types

{% tabs %}
{% tab title="User-Initiated Conversations" %}
**Free**: When a customer messages you first, the conversation is free for 24 hours. You can send unlimited messages during this window without charges.

**When it starts**: The moment the customer sends their first message.
**Duration**: 24 hours from the customer's last message.

**Best for**: Customer support, inquiries, and ongoing conversations.
{% endtab %}

{% tab title="Business-Initiated Conversations" %}
**Charged**: When you start a conversation using a Message Template, this creates a billable conversation.

**Charges apply**: Based on your WABA pricing tier and the conversation category (Marketing, Utility, Authentication, Service).

**Duration**: 24 hours from when you send the template message.

**Best for**: Outbound marketing, transactional updates, and notifications.
{% endtab %}
{% endtabs %}

## Conversation Categories

The cost of a business-initiated conversation depends on its category:

| Category | Use Case | Typical Cost | Approval Time |
|----------|----------|--------------|---------------|
| **Marketing** | Promotional messages, offers, updates | Higher cost | Longer (more scrutiny) |
| **Utility** | Transactional updates, receipts, notifications | Medium cost | Faster |
| **Authentication** | OTP codes, verification codes | Lower cost | Fastest |
| **Service** | Customer support, account updates | Lower cost | Moderate |

{% hint style="warning" %}
**Important**: Pricing varies by country and can change. Always refer to the [official WhatsApp Business API pricing documentation](https://developers.facebook.com/docs/whatsapp/pricing) for the most current rates.
{% endhint %}

## Understanding Costs

### Factors That Affect Pricing

1. **Conversation Category**: Marketing templates typically cost more than Utility or Service templates.
2. **Country/Region**: Different countries have different pricing tiers.
3. **Volume**: Some plans offer volume discounts for high message volumes.
4. **Account Type**: Verified businesses may have different pricing structures.

### Cost Optimization Tips

- **Prefer User-Initiated**: Encourage customers to message you first to start free conversations.
- **Choose Right Category**: Use Utility or Service categories when possible instead of Marketing for lower costs.
- **Respond Quickly**: Maintain active conversations within the 24-hour window to avoid template costs.
- **Batch Messages**: When using templates, send related messages within the same 24-hour conversation window.

## Important behavior to know

- **Conversation-Based**: You're charged per conversation, not per message. Multiple messages within the same 24-hour conversation count as one charge.
- **Free Window**: User-initiated conversations are free for 24 hours, allowing unlimited messages.
- **Template Required**: Business-initiated conversations always require a Message Template and are always charged.
- **Regional Pricing**: Costs vary significantly by country. Check official pricing for your region.

## Common issues & solutions

- **Unexpected Charges**: Review your conversation history. Business-initiated conversations using templates are always charged, even if the customer doesn't reply.
- **High Costs**: Focus on user-initiated conversations (free) and use templates only when necessary. Choose lower-cost categories (Utility, Service) when possible.
- **Unclear Pricing**: Refer to the [official WhatsApp pricing documentation](https://developers.facebook.com/docs/whatsapp/pricing) for your country's current rates.
- **Template Costs**: Remember that sending a template starts a billable conversation, regardless of whether the customer responds.

## Best practice 💡

- **Maximize Free Conversations**: Set up quick responses and automation to maintain active user-initiated conversations.
- **Strategic Template Use**: Reserve Marketing templates for important promotions. Use Utility or Service templates for routine updates.
- **Monitor Usage**: Regularly review your messaging costs and adjust your strategy accordingly.
- **Understand Categories**: Choose the appropriate template category to balance cost and approval speed.

## Related Documentation

- [Service Window](./service-window.md) - Learn how to maintain free messaging windows
- [Message Template Types](./message-template-types.md) - Understand different template categories and their costs
- [Messaging Limits & Quality](./messaging-limits-quality.md) - Learn about account tiers and how they affect your messaging capacity
- [Message Templates](../message-templates.md) - Learn how to create templates in Luluchat
- [Official WhatsApp Pricing](https://developers.facebook.com/docs/whatsapp/pricing) - Current pricing information by country
