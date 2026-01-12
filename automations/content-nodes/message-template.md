# Content: Message Template

## What is the Message Template Node?
This node allows you to send pre-approved official **WhatsApp Business API (WABA)** templates. These are mandatory for initiating conversations or messaging customers who haven't responded in more than 24 hours.

## When to use it?
- **Broadcasting**: Sending marketing messages to a list of contacts.
- **Re-engagement**: Following up with a customer after the 24-hour window has closed.
- **Notifications**: Automated alerts for orders, bookings, or shipping updates.

## How to set it up (Step by Step)
1. In the Message Flow Editor, click **Add Node (+) > Content > Message Template**.
2. Click the node to select from your list of approved templates.
3. If your template has variables (e.g., `{{1}}`), map each variable to a contact's **Custom Attribute** or type a static value.
4. If your template has interactive buttons (CTA or Quick Reply), you can link them to the next steps in your flow.

📸 Screenshot placeholder:
> [Screenshot: Message Template node showing variable mapping and button links]

## Important behavior to know
- **WABA Only**: This node is only visible and functional for WhatsApp Cloud accounts.
- **Pre-Approval Required**: You can only select templates that have already been approved by Meta. See the [Message Templates Library](../../message-templates.md) for how to create them.
- **Mapping Matters**: Ensure your variables are mapped correctly, or the message might fail to send.

## Best practice 💡
- **Fallback Logic**: Always have a template ready for re-engaging customers who dropped out of a conversation.
- **Personalized Variables**: Map variables to the customer's name or specific order details to increase relevancy.
