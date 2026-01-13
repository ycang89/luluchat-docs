# Shopify Integration

## What is Shopify Integration?

Shopify Integration allows you to connect your Shopify store with Luluchat, enabling you to automatically send WhatsApp messages to customers based on Shopify events like new orders, order fulfillments, or customer updates.

## When does it trigger?

* When you want to send automated WhatsApp messages to customers based on Shopify store events (orders, fulfillments, customer updates).
* When you need to sync customer data between Shopify and Luluchat.

## Prerequisites

* You must have a Shopify account
* You will need to generate an Admin API Access Token from your Shopify account

## How to set it up (Step by Step)

### Part 1: Generate Shopify Admin API Access Token

{% stepper %}
{% step %}
#### Sign Up or Log In to Shopify

Sign up or log in to your Shopify account at [https://www.shopify.com/](https://www.shopify.com/).

📸 Screenshot placeholder:

> \[Screenshot: Shopify login page]
{% endstep %}

{% step %}
#### Navigate to Apps and Sales Channels

Log in to your Shopify account, then go to **Settings** > **Apps and sales channels**.

<figure><img src="../../.gitbook/assets/Screenshot 2023-07-04 at 8.35.01 PM.png" alt=""><figcaption><p>Go to Settings</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2023-07-04 at 8.35.13 PM.png" alt=""><figcaption><p>Go to Apps and sales channels</p></figcaption></figure>
{% endstep %}

{% step %}
#### Create a New App

Click on **Develop Apps**, then click **Create an app**.

<figure><img src="../../.gitbook/assets/Screenshot 2023-07-04 at 8.35.42 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Name Your App

Give the app a **name** (e.g., "Luluchat Integration") and click **Create App**.

<figure><img src="../../.gitbook/assets/Screenshot 2023-07-04 at 8.36.02 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Configure Admin API Scopes

Click on **Configure Admin API scopes**.

<figure><img src="../../.gitbook/assets/Screenshot 2023-07-04 at 8.36.13 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Grant Required Access Scopes

**Grant access scope** to this app. Below are the access scopes needed. Use the search field to find each scope and tick the checkbox:

* read\_orders
* read\_fulfillments
* read\_payment\_terms
* read\_customers
* read\_draft\_order
* read\_order\_edits
* read\_third\_party\_fulfillment\_orders
* read\_assigned\_fulfillment\_orders

<figure><img src="../../.gitbook/assets/Screenshot 2023-07-04 at 8.36.42 PM.png" alt=""><figcaption></figcaption></figure>

You should have **8 selected scopes** at the end. Click the **Save** button to save the scope changes.

<figure><img src="../../.gitbook/assets/Screenshot 2023-07-04 at 8.37.41 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Install the App

Click on the **Install app** button to install this custom app to your Shopify store.

<figure><img src="../../.gitbook/assets/Screenshot 2023-07-04 at 8.38.07 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2023-07-04 at 8.38.19 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Reveal and Copy the Admin API Access Token

Click on the **Reveal token** button once. This will display your **Admin API Access Token**. Be sure to **copy the token** and securely store it for future use when connecting Luluchat.

{% hint style="warning" %}
**Important**: Copy and save this token immediately. You won't be able to see it again after closing this page.
{% endhint %}

<figure><img src="../../.gitbook/assets/Screenshot 2023-07-04 at 8.38.30 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

### Part 2: Connect Shopify in Luluchat

{% stepper %}
{% step %}
#### Access the Apps Section

To access this module, in the side navigation menu, click **Apps**. Alternatively, go to `Settings` > `Account Management` > `Integration` and scroll to the Apps section.

📸 Screenshot placeholder:

> \[Screenshot: Apps section in Integration settings]
{% endstep %}

{% step %}
#### Click on Shopify App

Click on the **Shopify** app card to open the connection page.

<figure><img src="../../.gitbook/assets/Screenshot 2023-07-04 at 8.22.39 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Enter Your Shopify Credentials

Enter the **Admin API Access Token** you copied from Shopify and your **Shopify URL** (just the store name, without .myshopify.com). Once you have filled in the required information, click on the **Connect** button.

<figure><img src="../../.gitbook/assets/Screenshot 2023-07-04 at 8.23.25 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

## What happens after it triggers?

* **Connection Established**: Your Shopify store is now connected to Luluchat.
* **Event Sync**: Shopify events (orders, fulfillments, customer updates) can now trigger actions in Luluchat.
* **Data Available**: Customer and order data from Shopify becomes available for use in Message Flows and automations.

## Important behavior to know

* **Token Security**: Your Admin API Access Token is sensitive information. Keep it secure and never share it publicly.
* **Required Scopes**: All 8 access scopes must be granted for the integration to work properly.
* **Store URL Format**: Enter only your store name (e.g., "mystore" for mystore.myshopify.com), not the full URL.
* **Reconnection**: If you need to reconnect, you can use the same token or generate a new one from Shopify.

## Common issues & solutions

* **Connection failed**: Verify that you copied the entire Admin API Access Token correctly without any extra spaces. Ensure all 8 required scopes are granted in Shopify.
* **Token not working**: Check that the token hasn't been revoked in Shopify. You may need to generate a new token if the old one was deleted.
* **Events not triggering**: Ensure the integration is active and that you've configured the event settings in the App Settings page after connecting.

## Best practice 💡

* **Secure Token Storage**: Store your Admin API Access Token in a secure password manager.
* **Regular Audits**: Periodically review your connected apps in Shopify to ensure only necessary integrations are active.
* **Test Events**: After connecting, test that Shopify events are properly triggering your Luluchat automations.
* **Monitor Usage**: Keep an eye on your Shopify API usage to ensure you're within your plan limits.

## Related Documentation

* [Integration Settings](integration.md) - Learn how to manage your integrations
* [Message Flows](../automations/message-flows.md) - Learn how to create automations triggered by Shopify events
