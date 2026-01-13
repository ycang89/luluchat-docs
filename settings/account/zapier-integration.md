# Zapier Integration

## What is Zapier Integration?
Zapier Integration allows you to connect Luluchat with thousands of other apps and services through Zapier's automation platform. You can trigger Message Flows in Luluchat based on events from other apps (like new Calendly bookings, Shopify orders, or Google Sheets updates).

## When does it trigger?
- When an event occurs in a connected app (trigger) and you've configured Zapier to send that data to Luluchat.
- When you want to automate sending WhatsApp messages through Luluchat based on actions in other platforms.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
### Accept the Luluchat Invitation in Zapier

To start using Luluchat in Zapier, you need to accept the Luluchat invitation. Click the link below to accept the invitation and start building your own Zap:

**Luluchat Invitation**: [https://zapier.com/developer/public-invite/186610/ed983254887d7d19937a08a198b5f5f9/](https://zapier.com/developer/public-invite/186610/ed983254887d7d19937a08a198b5f5f9/)

<figure><img src="../../.gitbook/assets/Screenshot 2024-07-12 at 2.14.22 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Create a New Zap

In Zapier, click **Create Zap** to start building a new automation. Choose your trigger app (the app that will start the automation). For example, you might choose Calendly for new booking events.

<figure><img src="../../.gitbook/assets/Screenshot 2024-07-12 at 1.01.01 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Add Luluchat as an Action

After setting up your trigger, click the **plus icon** to **Add a Step**. Search for "luluchat" in the app search field.

<figure><img src="../../.gitbook/assets/Screenshot 2024-07-12 at 1.01.16 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Choose Send Message Flow Event

In the Event Selection, choose **Send Message Flow** as the action you want Luluchat to perform.

<figure><img src="../../.gitbook/assets/Screenshot 2024-07-12 at 1.01.29 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Connect Your Luluchat Account

Zapier will prompt you to connect your account. A popup will ask for your **Zapier API Key**.

To find your Zapier API Key:
1. Go to `Settings` > `Account Management` > `Integration` in your Luluchat account.
2. Copy the **Zapier API Key** from the Integration settings page.
3. Paste the key into the Zapier popup and proceed.

<figure><img src="../../.gitbook/assets/Screenshot 2024-07-12 at 1.02.05 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2024-07-12 at 1.02.26 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2024-07-12 at 1.02.48 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Configure Your Message Flow in Luluchat

Before completing the Zap setup, ensure your Message Flow is ready in Luluchat:

1. Go to `Automations` > `Message Flows` in Luluchat.
2. Create or select the Message Flow you want to trigger from Zapier.
3. In the **Starting Step**, add a **Webhook** trigger. This opens the connection for Zapier to call your flow.

<figure><img src="../../.gitbook/assets/Screenshot 2024-07-12 at 1.03.10 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2024-07-19 at 3.34.14 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Select Your Message Flow in Zapier

Back in Zapier, in the action configuration:
1. Select the Message Flow you created in Luluchat from the dropdown.
2. Select the phone number from the data provided by your trigger (for example, if using Calendly, select the phone number field from the Calendly booking data).

<figure><img src="../../.gitbook/assets/Screenshot 2024-07-12 at 1.04.35 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2024-07-12 at 1.04.58 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Test and Publish Your Zap

You can test your integration at this step to verify it works correctly, or skip the test and publish it for production use.

<figure><img src="../../.gitbook/assets/Screenshot 2024-07-12 at 1.05.33 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2024-07-12 at 1.05.48 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

## What happens after it triggers?
When your Zap runs:
- The trigger event (e.g., new Calendly booking) sends data to Zapier.
- Zapier calls your Luluchat Message Flow via the webhook.
- Your Message Flow executes and sends the configured messages to the specified phone number.
- The contact receives the automated messages you've set up in the flow.

## Important behavior to know
- **Webhook Required**: Your Message Flow must have a Webhook trigger in the Starting Step for Zapier to be able to call it.
- **Phone Number Format**: Ensure the phone number from your trigger app is in the correct format (with country code, e.g., +60123456789).
- **Message Flow Must Be Published**: Only published Message Flows will appear in Zapier's dropdown. Draft flows cannot be triggered.
- **API Key Security**: Keep your Zapier API Key secure. If it's compromised, you can regenerate it in the Integration settings.

## Common issues & solutions
- **Message Flow not appearing in Zapier**: Ensure your Message Flow is published (not in draft) and has a Webhook trigger configured in the Starting Step.
- **Zap not triggering**: Check that your trigger app is properly connected and the trigger conditions are met. Verify your Zap is turned on in Zapier.
- **Messages not sending**: Verify the phone number format is correct and that your Luluchat channel is connected and active.
- **API Key error**: Make sure you copied the entire API key from Luluchat without any extra spaces. If issues persist, try regenerating the key in Integration settings.

## Best practice 💡
- **Test First**: Always test your Zap with a sample event before publishing to ensure the data mapping is correct.
- **Use Clear Flow Names**: Name your Message Flows descriptively (e.g., "Welcome New Booking") so they're easy to identify in Zapier.
- **Map Data Carefully**: Double-check that you're mapping the correct fields from your trigger app to the phone number and any other required fields.
- **Monitor Your Zaps**: Regularly check your Zap history in Zapier to ensure automations are running successfully.

## Related Documentation
- [Integration Settings](./integration.md) - Learn how to manage your API keys and access tokens
- [Message Flows](../automations/message-flows.md) - Learn how to create and configure Message Flows
- [Webhook Trigger](../automations/steps/trigger.md#4-webhook-trigger) - Learn more about Webhook triggers
- [Webhook Trigger Developer Guide](../developer-guide/webhook-trigger.md) - Technical implementation details for developers
