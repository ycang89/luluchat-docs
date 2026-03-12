# Connect your Channel

## What is Channel Connection?

Connecting your channel links your WhatsApp account (Personal, Cloud, or Coexistence) to Luluchat. This allows you to manage conversations, run automations, and send broadcasts directly from the platform.

## When does it trigger?

* When you first open `Inbox` and no channel is connected.
* When your existing channel is disconnected or requires re-authentication.

## How to open the Connect Channel page

{% stepper %}
{% step %}
**Open Inbox**

Click `Inbox` in the left menu. If your channel is not yet connected, you will automatically be directed to the **Connect your Channel** page.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-13 at 5.40.48 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Choose your Channel Type**

Select the type of WhatsApp account you want to connect:

* WhatsApp Personal: For standard WhatsApp or WhatsApp Business app accounts.
* WhatsApp Cloud: For accounts using the official WhatsApp Business API (WABA).
* WhatsApp Coexistence: For setups where Personal and Cloud channels coexist in the same workspace.
{% endstep %}
{% endstepper %}

## Channel types

Use these dedicated guides for step‑by‑step instructions:

* [WhatsApp Personal](connect-whatsapp-personal.md)
* [WhatsApp Cloud](connect-whatsapp-cloud.md)
* [WhatsApp Coexistence](connect-whatsapp-coexistence.md)

Coming soon:

* Meta Messenger
* Instagram

## What happens after it triggers?

Once the status changes to `ready` for a channel, you can start receiving and sending messages. Your Message Flows and Broadcasts will now be able to fire for that channel.

If you connect multiple channels (for example, Personal and Cloud), each channel operates independently with its own contacts and conversations.

## Common issues & solutions

* **Channel not ready**: Re-open the Connect Channel screen and complete the connection flow for your selected channel type.
* **Channel disconnected**:
  * Check your registered WhatsApp number for a disconnection notification message from Luluchat (for Personal channels).
  * Re-scan the QR code or re‑authenticate with Facebook, depending on your channel type.
  * If disconnected due to inactivity, log in to your primary phone's WhatsApp (Personal) or re‑authorize via Facebook (Cloud) and reconnect the channel.
* **Sync taking too long**:
  * If you have a large number of contacts, wait up to 15 minutes for the initial sync to complete.
  * Check your internet connection speed – a slow connection will delay the sync process.
* **Connection lost frequently**:
  * Ensure your phone (for Personal channels) maintains a stable internet connection.
  * Make sure you're using the latest version of WhatsApp.
* **Can't add more channels**:
  * Check if you've reached your plan's channel limit. You may need to upgrade your plan to add more channels.
  * Click "Need More Channel?" to view upgrade options.
  * Contact support if you believe you should have access to more channels.

{% hint style="success" %}
**Best practice**

* Connect only the channel types you actually need (Personal, Cloud, or both in Coexistence) so routing stays clear.
* Monitor the connection status in the Inbox header regularly to ensure your automations are active.
* Maintain a stable internet connection on your primary phone (Personal) or server (Cloud) during the connection process and while using Luluchat.
* Set reminders to periodically review channel health and re‑authenticate if needed.
{% endhint %}
