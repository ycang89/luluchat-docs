# Shopify Webhook Configuration

After you create and connect Shopify in Luluchat, you can configure which events you want to enable in the [Shopify App Details page](https://app.luluchat.io/apps/details/shopify).

## Available Events

The following events require webhook configuration in Shopify:

1. **Order Updated Notification** - Triggered when an order is edited or updated
2. **Order Paid Notification** - Triggered when an order payment is received
3. **Order Cancellation Notification** - Triggered when an order is cancelled
4. **Delivery Notification** - Triggered when a fulfillment is created (order is shipped)

**Note:** The **Payment Reminder Notification** does not require webhook configuration. This event is automatically triggered daily by the Luluchat system at 8:00 AM in your team's timezone to check for unpaid orders with payment due dates matching the current date.

## Event Configuration

For each event, you can configure:

* **Is Enabled** - Toggle to enable or disable the event
* **WhatsApp Number for Notifications** - Internal notification number for staff members. This is used to send internal notifications when the event is triggered.
* **Notification Message** - Internal message template for staff notifications (e.g., "1 order created. please follow up"). This message will be sent to the configured WhatsApp number when the event occurs.

## Setting Up Webhooks in Shopify

To configure webhooks in Shopify, follow these steps:

{% stepper %}
{% step %}
**Access Shopify Webhooks**

1. Log in to your Shopify admin panel
2. In the search bar at the top, search for **"webhooks"**
3. Click on the first result to access the Webhooks settings page

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-11 at 8.42.13 PM.png" alt=""><figcaption></figcaption></figure>

> \[Screenshot: Shopify admin search bar with "webhooks" search term]

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-11 at 8.42.39 PM.png" alt=""><figcaption></figcaption></figure>

> \[Screenshot: Shopify admin first matching webhooks page]
{% endstep %}

{% step %}
**Create Webhook for Order Paid Notification**

1.  Click **"Create webhook"** button

    <figure><img src="../../.gitbook/assets/Screenshot 2026-02-11 at 9.19.12 PM.png" alt=""><figcaption></figcaption></figure>



    > \[Screenshot: Click create webhook]


2. In the **Event** dropdown, select **"Order payment"**
3.  Copy the webhook endpoint URL from Luluchat (found in the Shopify App Details page for the **Order Paid Notification event**)<br>

    <figure><img src="../../.gitbook/assets/Screenshot 2026-02-11 at 9.22.40 PM.png" alt=""><figcaption></figcaption></figure>



    > \[Screenshot: Copy the webhook endpoint URL]


4.  Paste the webhook endpoint URL into the **URL** field<br>

    <figure><img src="../../.gitbook/assets/Screenshot 2026-02-11 at 8.43.34 PM.png" alt=""><figcaption></figcaption></figure>



    > \[Screenshot: Paste the webhook endpoint URL into the **URL** field]


5. Click **"Save"**
{% endstep %}

{% step %}
**Create Webhook for Order Cancellation Notification**

1. Click **"Create webhook"** button
2. In the **Event** dropdown, select **"Order cancellation"**
3.  Copy the webhook endpoint URL from Luluchat (found in the Shopify App Details page for the **Order Cancellation Notification event**)<br>

    <figure><img src="../../.gitbook/assets/Screenshot 2026-02-11 at 9.24.58 PM.png" alt=""><figcaption></figcaption></figure>



    > \[Screenshot: Copy the webhook endpoint URL]


4.  Paste the webhook endpoint URL into the **URL** field<br>

    <figure><img src="../../.gitbook/assets/Screenshot 2026-02-11 at 9.30.07 PM.png" alt=""><figcaption></figcaption></figure>



    > \[Screenshot: Paste the webhook endpoint URL into the **URL** field]


5. Click **"Save webhook"**
{% endstep %}

{% step %}
**Create Webhook for Delivery Notification**

1. Click **"Create webhook"** button
2. In the **Event** dropdown, select **"Fulfillment creation"**
3.  Copy the webhook endpoint URL from Luluchat (found in the Shopify App Details page for the **Delivery Notification event**)<br>

    <figure><img src="../../.gitbook/assets/Screenshot 2026-02-11 at 9.25.12 PM.png" alt=""><figcaption></figcaption></figure>



    > \[Screenshot: Copy the webhook endpoint URL]


4.  Paste the webhook endpoint URL into the **URL** field<br>

    <figure><img src="../../.gitbook/assets/Screenshot 2026-02-11 at 9.31.32 PM.png" alt=""><figcaption></figcaption></figure>



    > \[Screenshot: Paste the webhook endpoint URL into the **URL** field]


5. Click **"Save webhook"**
{% endstep %}

{% step %}
**Create Webhook for Order Updated Notification**

1. Click **"Create webhook"** button
2. In the **Event** dropdown, select **"Order edit"**
3.  Copy the webhook endpoint URL from Luluchat (found in the Shopify App Details page for the **Order Updated Notification event**)<br>

    <figure><img src="../../.gitbook/assets/Screenshot 2026-02-11 at 9.25.30 PM.png" alt=""><figcaption></figcaption></figure>



    > \[Screenshot: Copy the webhook endpoint URL]


4.  Paste the webhook endpoint URL into the **URL** field<br>

    <figure><img src="../../.gitbook/assets/Screenshot 2026-02-11 at 9.32.23 PM.png" alt=""><figcaption></figcaption></figure>



    > \[Screenshot: Paste the webhook endpoint URL into the **URL** field]


5. Click **"Save webhook"**
{% endstep %}

{% step %}
**At the end you should have 4 webhooks configured**

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-11 at 8.49.31 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

## Shopify Event to Luluchat Event Mapping

| Shopify Webhook Event | Luluchat Event                  |
| --------------------- | ------------------------------- |
| Order payment         | Order Paid Notification         |
| Order cancellation    | Order Cancellation Notification |
| Fulfillment creation  | Delivery Notification           |
| Order edit            | Order Updated Notification      |

## Payment Reminder Notification

The **Payment Reminder Notification** is a scheduled event that runs automatically and does not require webhook configuration. The Luluchat system checks for unpaid orders daily at **8:00 AM** in your team's timezone and sends payment reminders for orders with payment due dates matching the current date.

This event:

* Runs automatically once per day
* Does not require webhook setup in Shopify
* Checks for orders with `financial_status` of "unpaid" or "pending"
* Sends notifications for orders with payment due dates matching today's date

## Verifying Webhook Configuration

After setting up webhooks in Shopify:

1. Return to the [Shopify App Details page](https://app.luluchat.io/apps/details/shopify) in Luluchat
2. Ensure the events you want to use are enabled
3. Test the integration by performing the corresponding action in Shopify (e.g., create a test order payment to verify Order Paid Notification)
4. Check that notifications are received at your configured WhatsApp number for notifications

{% hint style="info" %}
**Tips:**

* Make sure to copy the correct webhook endpoint URL for each event from the Luluchat Shopify App Details page
* Each event requires a separate webhook configuration in Shopify
* The webhook endpoint URLs are unique to your Luluchat account and channel
* If you need to update a webhook URL, you can edit the webhook in Shopify or delete and recreate it
{% endhint %}

## Related Documentation

* [Shopify Integration](shopify-integration/) - Learn how to connect your Shopify store to Luluchat
* [Shopify App Event Trigger in Message Flows](../../automations/shopify-app-event-trigger/) - Learn how to configure Shopify events as triggers and use Shopify data in your messages
