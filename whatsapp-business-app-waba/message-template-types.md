# Message Template Types

## What are Message Templates?

Message Templates are pre-approved message formats that allow you to contact customers outside the 24-hour window or start new conversations. They must be created and approved through Meta's WhatsApp Manager before you can use them.

## Template Categories

WhatsApp categorizes templates into four types, each with different use cases, requirements, and costs:

{% tabs %}
{% tab title="Marketing" %}
**Purpose**: Promotional content, offers, announcements, newsletters.

**Use Cases**:
- New product launches
- Special promotions and sales
- Event invitations
- Newsletter updates
- Brand announcements

**Requirements**:
- Must clearly indicate promotional content
- Requires customer opt-in in many regions
- Higher approval scrutiny
- May require proof of customer consent

**Best For**: Reaching customers with promotional messages and marketing campaigns.

**Cost**: Typically the highest cost per conversation.

**Approval Time**: Longer (often 24 hours or more due to stricter review).
{% endtab %}

{% tab title="Utility" %}
**Purpose**: Transactional updates and important notifications.

**Use Cases**:
- Order confirmations
- Shipping updates and tracking
- Payment receipts
- Account statements
- Transaction notifications

**Requirements**:
- Must be transactional in nature
- Should provide important information about a transaction or account
- Usually faster approval
- Lower cost per conversation

**Best For**: Sending important transactional information that customers need to know.

**Cost**: Medium cost per conversation.

**Approval Time**: Faster (often approved within hours).
{% endtab %}

{% tab title="Authentication" %}
**Purpose**: Security and verification codes.

**Use Cases**:
- OTP (One-Time Password) codes
- Login verification codes
- Account verification codes
- Two-factor authentication

**Requirements**:
- Must be security-related
- Should only contain verification codes
- Fastest approval process
- Lowest cost per conversation

**Best For**: Sending security codes and verification numbers.

**Cost**: Lowest cost per conversation.

**Approval Time**: Fastest (often approved within minutes to hours).
{% endtab %}

{% tab title="Service" %}
**Purpose**: Customer support and account updates.

**Use Cases**:
- Support ticket updates
- Account status changes
- Appointment reminders
- Service notifications
- Account alerts

**Requirements**:
- Must be service-related
- Should provide updates about customer service or account status
- Moderate approval time
- Lower cost per conversation

**Best For**: Keeping customers informed about their account or support requests.

**Cost**: Lower cost per conversation.

**Approval Time**: Moderate (typically approved within a few hours).
{% endtab %}
{% endtabs %}

## Template Components

All message templates can include these components:

- **Header**: Optional image, video, or text at the top of the message
- **Body**: Main message content (can include variables like `{{1}}`, `{{2}}` for personalization)
- **Footer**: Optional text at the bottom (useful for disclaimers or company information)
- **Buttons**: Optional call-to-action buttons
  - Up to 3 buttons, OR
  - 1 quick reply button

## Choosing the Right Category

**Select Marketing when**:
- You're promoting products, services, or offers
- The message is primarily promotional
- You have customer opt-in/consent

**Select Utility when**:
- You're sending transaction-related information
- The message is about an order, payment, or account transaction
- The customer needs this information for their records

**Select Authentication when**:
- You're sending verification or security codes
- The message is purely for authentication purposes
- Speed of delivery is critical

**Select Service when**:
- You're providing customer support updates
- The message is about account status or service changes
- You're responding to a service request

{% hint style="warning" %}
**Important**: Choosing the wrong category can result in template rejection. Make sure your template content matches the selected category. Promotional content should never be in Utility, Authentication, or Service categories.
{% endhint %}

## Important behavior to know

- **Approval Required**: All templates must be approved by WhatsApp before use. Approval times vary by category.
- **Category Matching**: The template content must match the selected category. Mismatched content will be rejected.
- **Variables**: You can use variables (e.g., `{{1}}`, `{{2}}`) in templates, which you'll fill in when sending the message.
- **One-Time Use**: Templates are reusable - once approved, you can use them multiple times.
- **Quality Score**: Your template quality affects approval speed and account standing.

## Common issues & solutions

- **Template Rejected**: Review Meta's template guidelines. Common issues include:
  - Unclear category selection
  - Promotional content in non-Marketing templates
  - Formatting errors
  - Missing required information
- **Wrong Category**: Ensure your template content matches the category. Marketing content must be in Marketing category.
- **Slow Approval**: Authentication and Utility templates typically approve faster. Marketing templates take longer due to stricter review.
- **Variables Not Working**: Ensure variables are properly formatted as `{{1}}`, `{{2}}`, etc., and that you're providing values when sending.

## Best practice 💡

- **Choose Right Category**: Select the appropriate category from the start to avoid rejection and delays.
- **Use Lower-Cost Categories**: When possible, use Utility, Service, or Authentication instead of Marketing to reduce costs.
- **Keep It Simple**: Clear, concise templates approve faster than complex ones.
- **Test Variables**: Always test that your variable mapping works correctly before sending to many customers.
- **Review Guidelines**: Before creating templates, review Meta's template guidelines to ensure compliance.

## Related Documentation

- [Service Window](./service-window.md) - Learn when templates are required
- [Charging & Pricing](./charging-pricing.md) - Understand how template categories affect costs
- [Messaging Limits & Quality](./messaging-limits-quality.md) - Learn how template quality affects your account rating
- [Message Templates](../message-templates.md) - Learn how to create and manage templates in Luluchat
- [Official Template Guidelines](https://developers.facebook.com/docs/whatsapp/business-platform/guides/send-messages) - Meta's official template documentation
