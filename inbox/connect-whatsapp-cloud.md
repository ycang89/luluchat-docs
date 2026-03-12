# WhatsApp Cloud

## What is WhatsApp Cloud connection?

Connecting a **WhatsApp Cloud** channel links your WhatsApp Business API (WABA) account to Luluchat via Meta’s official Cloud API. This is recommended if you:

* Need higher‑volume, API‑based messaging.
* Use approved message templates (for outbound messages outside the 24‑hour window).
* Manage WhatsApp under a Facebook Business account.

Use this option if you already have, or plan to create, a WhatsApp Business API (Cloud) setup in Meta.

## When does it trigger?

* When you first open `Inbox` and choose **WhatsApp Cloud** on the Connect Channel page.
* When an existing Cloud channel is disconnected, invalid, or requires re‑authentication.

## How to set it up (Step by Step)

{% hint style="info" %}
**Learn More**: For detailed information about WhatsApp Business App (WABA) features and configuration, see the [WABA Documentation](../whatsapp-business-app-waba/index.md).
{% endhint %}

{% stepper %}
{% step %}
**Open Inbox and go to Connect Channel**

1. Click `Inbox` in the left menu.
2. If no channel is connected or you want to add a new one, open the **Connect your Channel** page.
3. Select **WhatsApp Cloud** as the channel type.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-13 at 5.40.48 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Authenticate with Facebook**

1. Click **Continue with Facebook** (or similar CTA) on the Connect Channel screen.
2. Log in with your **Facebook Business** account that manages your WABA.
3. Grant Luluchat the requested permissions so it can access your WhatsApp Business assets.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-13 at 5.59.41 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Select Phone Number**

1. After authentication, Luluchat will list the phone numbers available under your WABA.
2. Choose the specific phone number you want to connect as a channel.
3. Confirm your selection to proceed.
{% endstep %}

{% step %}
**Enter Verification PIN**

1. Create or confirm a **verification PIN** for this channel connection. You will need to create the PIN yourself; it is not an OTP received from Meta messages.
2. Keep this PIN safe – you may need it again when re‑authenticating the channel.
{% endstep %}

{% step %}
**Wait for Sync**

Once connected, Luluchat begins syncing your contacts and conversations for the selected WABA phone number.

* If you have many contacts or conversations, initial sync can take up to 15 minutes.
* You can monitor channel status from the Inbox header or channel settings.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-13 at 6.04.04 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

## What happens after it triggers?

Once the WhatsApp Cloud channel status is `ready`:

* Luluchat can send and receive messages for that phone number via the Cloud API.
* You can use **Message Flows** and **Broadcasts** with WABA‑specific behavior:
  * Template messages for starting conversations outside the 24‑hour service window.
  * Session messages (within 24 hours of last user message).
* Channel status and errors surface in places like Broadcast queues and flow logs.

## Important behavior to know (Cloud / WABA)

{% hint style="info" %}
**Important behavior to know**

* **Multiple Channels**: Depending on your plan, you can connect multiple Cloud channels (different WABA numbers) and/or Personal channels. Each channel has independent conversations and contacts.
* **Channel Limits**: Your subscription plan controls how many channels you can connect. Contact support if you need additional capacity.
* **24‑Hour Service Window**: For non‑template messages, WABA only allows sending within 24 hours of the last message from the customer. Outside this window, you must use an approved message template.
* **Template Approval**: Templates must be created and approved in Meta before you can use them in Luluchat.
* **Quotas and Tiers**: Meta may enforce messaging quotas per WABA. Exceeding these can temporarily block additional messages.
{% endhint %}

## Common issues & solutions (Cloud)

* **Failed to register (WABA)**:
  * Ensure your Facebook Business account has the correct permissions for the selected WABA.
  * Confirm that the phone number is not already used by another WABA integration that conflicts with Luluchat.
* **Channel is not ready / Invalid Channel Data**:
  * Reconnect the channel from the Connect Channel page.
  * Verify in Meta Business settings that your WABA and phone number are active and correctly configured.
* **Messages failing with 24‑hour window errors**:
  * Use approved **template messages** for contacts who have not interacted in the last 24 hours.
  * Review error details in the Broadcast Message Queue or logs.
* **Insufficient quota / tier limits**:
  * Check your WABA messaging limits in Meta Business Manager.
  * Reduce volume, wait for quota reset, or upgrade your tier as needed.
* **Sync taking too long**:
  * Large accounts can take longer for the initial import.
  * Make sure your server connection (and Luluchat) have stable network connectivity.

## Error codes (WhatsApp Business Platform)

Sometimes a message cannot be sent from your WhatsApp Cloud channel because the WhatsApp Business Platform (Meta) returns an error.

When this happens:

* Luluchat displays the **error code and message** returned by Meta in places like Broadcast Message Queue, flow logs, or channel status.
* You can look up what the code means and how to fix it in Meta’s official error code reference: [WhatsApp Business Platform Error Codes](https://developers.facebook.com/documentation/business-messaging/whatsapp/support/error-codes).

Use the Meta list to understand whether the issue is quota, template, permission, or something else, then apply the suggested resolution and retry from Luluchat if appropriate.

{% hint style="success" %}
**Best practice (WhatsApp Cloud)**

* Keep your **Facebook Business** and WABA configuration clean – remove unused numbers and integrations to avoid conflicts.
* Use **message templates** for outbound campaigns and re‑engagement to stay compliant with WABA rules.
* Monitor error messages in Broadcast queues and flow logs to quickly spot quota or template issues.
* Plan your sending volumes around Meta’s quotas to avoid sudden drops in deliverability.
{% endhint %}
