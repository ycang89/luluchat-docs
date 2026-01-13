# Trigger

## What is the Trigger Step?

The Trigger (or Starting Step) is the entry point of your Message Flow. It defines **when** and **how** your automation begins. Every flow must have a Starting Step, and you can configure one or more triggers to activate it.

## When does it trigger?

The flow starts when any of the configured triggers fire:

* A customer sends a message matching your **Keyword** rules
* A customer clicks a **WhatsApp Link** you've shared
* An external app sends an **App Event** (like Shopify order created)
* An external system sends a **Webhook** request to Luluchat

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Open the Starting Step

Every new flow starts with a **Starting Step** already on the board. Click on it to open the trigger configuration panel.

📸 Screenshot placeholder:

> \[Screenshot: Starting Step node on the flow board with configuration panel open]
{% endstep %}

{% step %}
#### Add a Trigger

Click one of the trigger buttons to add it:

* Keyword: For text-based message matching
* WhatsApp Link: For shareable clickable links
* App Event: For integrations with external apps
* Webhook: For custom external system triggers

📸 Screenshot placeholder:

> \[Screenshot: Starting Step configuration showing the four trigger type buttons]
{% endstep %}

{% step %}
#### Configure Your Trigger

Each trigger type has its own configuration. See the sections below for detailed setup instructions.
{% endstep %}

{% step %}
#### Add Multiple Triggers (Optional)

You can add multiple triggers to a single flow. The flow will start if **any** of them fire (e.g., the flow starts if the user types "Hi" OR clicks a specific WhatsApp Link).

📸 Screenshot placeholder:

> \[Screenshot: Starting Step showing multiple triggers configured]
{% endstep %}
{% endstepper %}

***

## Trigger Types Explained

### 1. Keyword Trigger

**What it does**: Starts the flow when a customer's message matches specific words or phrases you define.

**How to configure**:

1. Click **Keyword** in the Starting Step configuration.
2. Choose a **match condition** (see Keyword Match Rules below).
3. Enter the keyword(s) you want to match.
4. The flow will start automatically when a customer's message matches your rules.

📸 Screenshot placeholder:

> \[Screenshot: Keyword trigger configuration modal with condition selector and keyword input]

**Keyword Match Rules**:

* **is** (exact match): The message must match the keyword exactly. For example, if you set "I want to cancel my order", it will only trigger if the customer sends that exact phrase.
* **contain**: The message includes **any** of the keywords you list. For example, if you set "sales" and "discount", the flow triggers if the message contains either word.
* **contain all**: The message must include **all** keywords you list. For example, if you set "air fryer" and "Telfa", the flow only triggers if both words appear in the message.
* **begin with**: The message starts with the keyword. For example, if you set "help", messages like "Help, I can't log in" will trigger.
* **end with**: The message ends with the keyword. For example, if you set "thanks", messages ending with "thanks" will trigger.

**Important behavior to know**:

* Keywords are case-insensitive ("Hello" and "hello" are treated the same).
* You can add multiple keywords to a single trigger.
* If multiple flows have overlapping keywords, the first matching flow will trigger.

***

### 2. WhatsApp Link Trigger

**What it does**: Starts the flow when a customer clicks a special WhatsApp link you've created and shared.

**How to configure**:

1. Click **WhatsApp Link** in the Starting Step configuration.
2. Give your link a **Label** (e.g., "Summer Promotion Link").
3. Optionally set a **Pre-filled Message** that appears when the customer clicks the link.
4. Copy the generated link and share it on social media, emails, or your website.

📸 Screenshot placeholder:

> \[Screenshot: WhatsApp Link configuration showing label, message fields, and generated link]

**When to use it**:

* **Marketing Campaigns**: Share links in email newsletters or social media posts.
* **QR Codes**: Generate QR codes from these links for print materials or physical locations.
* **Trackable Entry Points**: See which link brought the customer to your flow.

**Important behavior to know**:

* Each WhatsApp Link trigger generates a unique URL.
* The link opens WhatsApp on the customer's phone with your pre-filled message (if configured).
* When they send that message (or any message), your flow starts.

***

### 3. App Event Trigger

**What it does**: Starts the flow automatically when a specific event happens in an integrated external app (like Shopify, ChatGPT, or other supported platforms).

**How to configure**:

1. Click **App Event** in the Starting Step configuration.
2. Select the **App** you want to integrate (e.g., Shopify).
3. Choose the **Event** you want to listen for (e.g., "Order Created", "Customer Registered").
4. Optionally map the event data to your **Custom Attributes** so you can use that information in your flow.

📸 Screenshot placeholder:

> \[Screenshot: App Event configuration showing app selector, event dropdown, and attribute mapping]

**When to use it**:

* **E-commerce**: Send order confirmations or shipping updates when a Shopify order is created.
* **User Onboarding**: Welcome new users when they register in your app.
* **Automated Notifications**: Trigger flows based on events in your business systems.

**Important behavior to know**:

* You need to have the app integration configured in your Luluchat account first.
* The event must include a customer's phone number to trigger the flow.
* You can map event data (like order ID or customer name) to Custom Attributes for use in your messages.

***

### 4. Webhook Trigger

**What it does**: Starts the flow when your external system sends an HTTP POST request to Luluchat's webhook URL.

**How to configure**:

1. Click **Webhook** in the Starting Step configuration.
2. Copy the **Webhook URL** provided by Luluchat.
3. Configure your external system to send a POST request to this URL with the customer's phone number.
4. Optionally map the webhook response data to your **Custom Attributes**.

📸 Screenshot placeholder:

> \[Screenshot: Webhook configuration showing the webhook URL and attribute mapping options]

**Webhook Requirements**:

* Your external system must send an **HTTP POST** request.
* The POST body **must include** `contact_number` (the customer's WhatsApp number).
* If webhook authentication is enabled in Settings, include the Authorization header with your API key.

**When to use it**:

* **Custom Integrations**: Connect Luluchat to your own internal systems or databases.
* **CRM Sync**: Trigger flows when a lead is created in your CRM.
* **Custom Business Logic**: Start automations based on events in your proprietary software.

**Important behavior to know**:

* **One Webhook per Flow**: Each flow can only have one webhook trigger.
* **Security**: Enable webhook authentication in Settings > Message Flows to protect your webhook URL.
* **Response Mapping**: Map webhook response fields to Custom Attributes to personalize your messages.

**For developers**: See the [Webhook Trigger Developer Guide](../../developer-guide/webhook-trigger.md) for technical implementation details, API requirements, and data formatting.

***

## What happens after it triggers?

Once any trigger fires, the flow immediately starts executing from the first step after the Starting Step. The customer will begin receiving messages or actions according to your flow design.

## Important behavior to know

* **First Node**: The Starting Step is always the first node executed in any flow.
* **No Incoming Links**: This node cannot have arrows pointing _to_ it; it only has an arrow pointing _from_ it to the next step.
* **Multiple Triggers**: You can add multiple triggers to one flow. The flow starts if **any** of them fire.
* **Trigger Limits**: Configure trigger limits in [Flow Settings](../message-flows-editor.md) to prevent the same flow from firing too frequently for the same customer.
* **Channel-Specific**: Triggers are tied to your connected WhatsApp channel. Ensure your channel is active for triggers to work.

## Common issues & solutions

* **Keyword not triggering**: Check that the match condition matches your test message exactly. Remember that "is" requires an exact match, while "contain" is more flexible.
* **WhatsApp Link not working**: Ensure the link is copied correctly and that the customer's phone has WhatsApp installed. The link must be opened on a device with WhatsApp.
* **App Event not firing**: Verify that the app integration is properly configured and that the event you selected is actually occurring in that app.
* **Webhook not received**: Check that your external system is sending a POST request (not GET) and that the `contact_number` field is included in the request body. Verify the webhook URL is correct. For technical details, see the [Webhook Trigger Developer Guide](../developer-guide/webhook-trigger.md).

## Best practice 💡

* **Use Specific Keywords**: Choose precise keywords to avoid conflicts. For example, use "cancel order" instead of just "cancel" to avoid triggering on unrelated messages.
* **Test Your Triggers**: Always test each trigger type with a real scenario before relying on it for important campaigns.
* **Combine Triggers**: Use multiple trigger types for the same flow to reach customers through different entry points (e.g., both a keyword and a WhatsApp Link).
* **Monitor Performance**: Check which triggers are most effective by reviewing your flow analytics to see which entry points bring the most engagement.
