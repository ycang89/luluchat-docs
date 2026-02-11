# Shopify App Event Trigger in Message Flows

This guide explains how to configure Shopify app events as triggers in your Message Flows and how to use Shopify custom attributes in your messages.

## What is Shopify App Event Trigger?

The Shopify App Event Trigger allows your Message Flow to automatically start when a specific event occurs in your Shopify store, such as when an order is paid, cancelled, shipped, or updated. This enables you to send automated WhatsApp messages to customers based on their Shopify order activity.

## Prerequisites

* You must have [Shopify Integration](../settings/account/shopify-integration) connected in Luluchat
* You must have [Shopify Webhooks configured](../settings/account/shopify-webhook-configuration) for the events you want to use
* You need to have created a Message Flow in Luluchat

## Available Shopify Events

You can configure the following Shopify events as triggers:

1. **Order Paid Notification** - Triggers when a customer's order payment is received
2. **Order Cancellation Notification** - Triggers when an order is cancelled
3. **Delivery Notification** - Triggers when a fulfillment is created (order is shipped)
4. **Order Updated Notification** - Triggers when an order is edited or updated
5. **Payment Reminder Notification** - Triggers daily at 8:00 AM for unpaid orders with due dates matching today

## How to Configure Shopify App Event Trigger

{% stepper %}
{% step %}
**Open Your Message Flow**

1. Go to **Message Flow** in the left menu
2. Create a new message flow or open an existing one
3. Click on the **Starting Step** (the first node in your flow)

📸 Screenshot placeholder:

> \[Screenshot: Message Flow editor with Starting Step selected]
{% endstep %}

{% step %}
**Add App Event Trigger**

1. In the Starting Step configuration panel, click on **App Event**
2. Select **Shopify** from the App dropdown
3. Choose the event you want to trigger the flow (e.g., "Order Paid Notification")

📸 Screenshot placeholder:

> \[Screenshot: Starting Step configuration showing App Event selected with Shopify app and event dropdown]
{% endstep %}

{% step %}
**Map Custom Attributes (Optional)**

1. If you want to store Shopify data in Custom Attributes for later use, click on **Map Attributes**
2. Select the Custom Attributes you want to populate
3. Map them to the corresponding Shopify placeholders (e.g., map "Order Number" custom attribute to `{{order.orderNumber}}`)
4. Click **Save** to confirm the mapping

📸 Screenshot placeholder:

> \[Screenshot: Attribute mapping interface showing Custom Attributes mapped to Shopify placeholders]
{% endstep %}

{% step %}
**Save Your Configuration**

1. Click **Save** to save your trigger configuration
2. Your flow will now automatically start when the selected Shopify event occurs

📸 Screenshot placeholder:

> \[Screenshot: Starting Step showing Shopify App Event trigger configured]
{% endstep %}
{% endstepper %}

## Using Shopify Custom Attributes in Messages

Once you've configured a Shopify App Event trigger, you can use Shopify data in your messages using placeholders. These placeholders will be automatically replaced with actual data from the Shopify event when the message is sent.

### Available Shopify Placeholders

#### Customer Information

* `{{customer.email}}` - Customer's email address
* `{{customer.name}}` - Customer's full name (first name + last name)

#### Order Information

* `{{order.id}}` - Shopify order ID
* `{{order.orderNumber}}` - Order number (display number)
* `{{order.email}}` - Order email address
* `{{order.currency}}` - Order currency code (e.g., USD, EUR)
* `{{order.dateCreated}}` - Order creation date (YYYY-MM-DD format)
* `{{order.dateCancelled}}` - Order cancellation date (if cancelled)
* `{{order.subtotal}}` - Order subtotal amount
* `{{order.tax}}` - Total tax amount
* `{{order.discount}}` - Total discount amount
* `{{order.lineItemsTotal}}` - Total line items price
* `{{order.total}}` - Total order amount
* `{{order.lineItems}}` - List of order line items (numbered list format)

#### Shipping Information

* `{{shipping.name}}` - Shipping recipient name
* `{{shipping.address}}` - Complete shipping address
* `{{shipping.total}}` - Shipping cost
* `{{shipping.trackingCompany}}` - Shipping carrier name
* `{{shipping.trackingNumber}}` - Tracking number(s)
* `{{shipping.trackingUrl}}` - Tracking URL(s)

#### Billing Information

* `{{billing.name}}` - Billing recipient name
* `{{billing.address}}` - Complete billing address

#### Delivery Information (for Delivery Notification events)

* `{{receiver.name}}` - Delivery recipient name

### How to Use Placeholders in Messages

1. **In Message Steps**: Simply type the placeholder directly in your message content
2. **In Custom Attributes**: Use placeholders when mapping data to custom attributes
3. **Case Sensitive**: Placeholders are case-sensitive, so make sure to use the exact format (e.g., `{{order.orderNumber}}` not `{{Order.OrderNumber}}`)

📸 Screenshot placeholder:

> \[Screenshot: Message step showing placeholder usage in message content]

## Example: Order Paid Notification Flow

Let's create a complete example flow that sends a confirmation message when an order is paid.

{% stepper %}
{% step %}
**Create the Flow**

1. Go to **Message Flow** and click **Create New Flow**
2. Name it "Order Confirmation"
3. Click on the **Starting Step**

📸 Screenshot placeholder:

> \[Screenshot: New message flow creation]
{% endstep %}

{% step %}
**Configure the Trigger**

1. Click **App Event** in the Starting Step
2. Select **Shopify** as the app
3. Choose **Order Paid Notification** as the event
4. Click **Save**

📸 Screenshot placeholder:

> \[Screenshot: App Event trigger configured for Order Paid Notification]
{% endstep %}

{% step %}
**Add a Message Step**

1. Click **Add Step** after the Starting Step
2. Select **Send Message** step
3. Compose your order confirmation message using Shopify placeholders

**Example Message:**

```
Hi {{customer.name}}! 👋

Thank you for your order! We've received your payment and your order is being processed.

📦 Order Details:
Order Number: {{order.orderNumber}}
Order Date: {{order.dateCreated}}
Total Amount: {{order.currency}} {{order.total}}

🛍️ Items Ordered:
{{order.lineItems}}

We'll send you another update when your order ships!

Thank you for shopping with us!
```

📸 Screenshot placeholder:

> \[Screenshot: Message step showing the order confirmation message with placeholders]
{% endstep %}

{% step %}
**Test Your Flow**

1. Save your flow
2. Make sure the flow is **Active**
3. Create a test order in Shopify and complete the payment
4. Verify that the message is sent with the correct order information

📸 Screenshot placeholder:

> \[Screenshot: Flow showing complete order confirmation flow with message step]
{% endstep %}
{% endstepper %}

### Example Message Output

When an order is paid, the customer will receive a message like this:

```
Hi John Smith! 👋

Thank you for your order! We've received your payment and your order is being processed.

📦 Order Details:
Order Number: #1001
Order Date: 2024-01-15
Total Amount: USD 125.50

🛍️ Items Ordered:
1. Blue Cotton T-Shirt
2. Black Jeans

We'll send you another update when your order ships!

Thank you for shopping with us!
```

## Mapping Custom Attributes

You can also map Shopify data to Custom Attributes so you can use them in other parts of your flow or in future conversations.

### How to Map Attributes

1. In the App Event trigger configuration, click **Map Attributes**
2. Select a Custom Attribute from your list (e.g., "Order Number", "Customer Name")
3. Choose the corresponding Shopify placeholder from the dropdown (e.g., `{{order.orderNumber}}`, `{{customer.name}}`)
4. Repeat for all attributes you want to map
5. Click **Save**

📸 Screenshot placeholder:

> \[Screenshot: Custom attribute mapping interface showing Order Number mapped to {{order.orderNumber}}]

### Using Mapped Custom Attributes

Once mapped, you can use these Custom Attributes in your messages using the standard Custom Attribute syntax:

* `{{Order Number}}` - Will display the order number from Shopify
* `{{Customer Name}}` - Will display the customer name from Shopify

**Note**: Custom Attributes use a different syntax (no dots, title case) compared to Shopify placeholders (with dots, camelCase).

## Important Behavior to Know

* **Phone Number Required**: The Shopify event must include a customer phone number for the flow to trigger. The system will look for the phone number in the order's billing address, shipping address, or customer profile.
* **Automatic Contact Creation**: If the customer doesn't exist in Luluchat, a new contact will be automatically created when the event triggers.
* **Real-time Triggering**: Events trigger in real-time when they occur in Shopify (except Payment Reminder which runs daily at 8:00 AM).
* **One Flow per Event**: You can have multiple flows with the same Shopify event trigger, but each will trigger independently.
* **Placeholder Availability**: Not all placeholders are available for all events. For example, shipping placeholders are only available for Delivery Notification events.

## Common Issues & Solutions

* **Flow not triggering**:
  * Verify that Shopify webhooks are properly configured in Shopify
  * Check that the event is enabled in the [Shopify App Details page](https://app.luluchat.io/apps/details/shopify)
  * Ensure the order has a valid phone number in the billing or shipping address
  * Verify that your Message Flow is active

* **Placeholders showing as empty**:
  * Check that the Shopify event actually contains the data you're trying to access
  * Some placeholders are only available for specific events (e.g., shipping info only for Delivery Notification)
  * Verify the placeholder syntax is correct (case-sensitive)

* **Custom Attributes not updating**:
  * Ensure you've mapped the attributes correctly in the trigger configuration
  * Check that the Custom Attribute data type matches the Shopify data type
  * Verify the mapping is saved in the trigger configuration

## Best Practice 💡

* **Test with Real Orders**: Always test your flows with actual Shopify orders to ensure placeholders work correctly
* **Use Appropriate Events**: Choose the right event for your use case (e.g., use Order Paid for payment confirmations, Delivery Notification for shipping updates)
* **Personalize Messages**: Use customer and order placeholders to make messages more personal and informative
* **Map Important Data**: Map frequently used data (like Order Number) to Custom Attributes for easier access in other flows
* **Keep Messages Concise**: While you have access to lots of data, keep messages concise and focused on the most important information

## Related Documentation

* [Shopify Integration](../settings/account/shopify-integration) - Learn how to connect Shopify to Luluchat
* [Shopify Webhook Configuration](../settings/account/shopify-webhook-configuration) - Learn how to configure webhooks for Shopify events
* [Message Flows](message-flows) - Learn about creating and managing message flows
* [Trigger Step](steps/trigger) - Learn about all trigger types available in message flows
