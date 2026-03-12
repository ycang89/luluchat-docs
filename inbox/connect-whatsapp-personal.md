# Connect WhatsApp Personal

## What is WhatsApp Personal connection?

Connecting a **WhatsApp Personal** channel links your standard WhatsApp or WhatsApp Business app account to Luluchat via WhatsApp’s multi‑device feature. This lets you:

* Receive and reply to conversations from the Inbox.
* Trigger Message Flows and automations.
* Use Broadcasts (subject to your plan and limits).

Use this option if you primarily use the WhatsApp or WhatsApp Business mobile app and do not have a WhatsApp Business API (WABA) account.

## When does it trigger?

* When you first open `Inbox` and no WhatsApp Personal channel is connected.
* When a previously connected Personal channel was disconnected or expired and you choose **WhatsApp Personal** on the Connect Channel page.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
**Open Inbox and go to Connect Channel**

1. Click `Inbox` in the left menu.  
2. If no channel is connected, you will be taken to the **Connect your Channel** page.  
3. Select **WhatsApp Personal** as the channel type.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-13 at 5.40.48 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Scan QR Code**

1. Luluchat will generate a WhatsApp QR code on screen.  
2. On your phone, open **WhatsApp** (or **WhatsApp Business**).  
3. Go to **Settings > Linked Devices**.  
4. Tap **Link a device** and scan the QR code shown in Luluchat.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-13 at 5.59.16 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Link with Phone Number (Alternative)**

If you cannot scan the QR code (for example, the camera is blocked or you’re on a remote device), use the phone‑number pairing option:

1. On the Connect Channel screen, click **Link with Phone Number**.  
2. Enter your WhatsApp phone number to receive a pairing code.  
3. On your phone, open WhatsApp and go to **Settings > Linked Devices > Link with Phone Number**.  
4. Enter the pairing code you received to complete the link.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-13 at 6.05.16 PM.png" alt=""><figcaption></figcaption></figure>

After entering your WhatsApp phone number, you will receive a notification prompting you to enter the pairing code. Follow the on‑screen instructions to complete the pairing process.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-13 at 6.06.05 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Check Syncing Status**

After connecting, WhatsApp starts syncing your contacts and messages to the linked device (Luluchat).

1. On your phone, open **WhatsApp**.  
2. Go to **Settings > Linked Devices**.  
3. Check the sync progress for your newly linked device.  
4. Wait for the sync to complete before heavily using Inbox, Message Flows, or Broadcasts.

📸 Screenshot placeholder:

> \[Screenshot: WhatsApp Linked Devices showing sync status]
{% endstep %}
{% endstepper %}

## What happens after it triggers?

Once the channel status changes to `ready` in Luluchat:

* New inbound messages to your WhatsApp number appear in `Inbox`.  
* You can reply directly from Luluchat and see messages on both your phone and Inbox.  
* Message Flows and Broadcasts targeting this channel can start sending (subject to your workspace and WhatsApp limits).

## Notes and limitations (WhatsApp Personal)

**Note:**

* Make sure your mobile phone has a stable internet connection.
* Keep the latest WhatsApp or WhatsApp Business app installed on your phone.
* If you have a very large number of contacts, the first sync can take up to 15 minutes. Wait before assuming something is wrong.
* You can check sync status in **Settings > Linked Devices** on your phone at any time.
* After you have connected WhatsApp to Luluchat, you must log in to your primary phone at least once every **14 days** to keep linked devices connected. If you don’t, WhatsApp automatically disconnects linked devices (including Luluchat).

## Common issues & solutions (Personal)

* **QR Code not loading**: Refresh the page to generate a new code and try again.
* **QR Code scanned but not connecting**:
  * Make sure your phone has a stable internet connection.
  * Confirm that multi‑device is enabled and WhatsApp is up to date.
* **Pairing via phone number fails**:
  * Ensure you entered the correct phone number and pairing code.
  * Try again after a few minutes in case of temporary network issues.
* **Channel disconnected**:
  * Check your registered WhatsApp number for a disconnection notification from Luluchat.
  * Re‑scan the QR code or re‑link via phone number.
  * If disconnected due to 14‑day inactivity, open WhatsApp on your primary phone and then reconnect the channel in Luluchat.
* **Sync taking too long**:
  * Large contact lists can take up to 15 minutes for the initial sync.
  * Verify that both your phone and Luluchat have stable internet connections.
* **Connection lost frequently**:
  * Ensure your phone’s Wi‑Fi or data connection is stable.
  * Keep WhatsApp updated to the latest version.

{% hint style="success" %}
**Best practice (WhatsApp Personal)**

* Use a **dedicated business phone** for your WhatsApp Personal channel to avoid accidental logouts and number changes.
* Periodically check **Settings > Linked Devices** on your phone to verify that the Luluchat device is still linked and syncing.
* Set a reminder every **10–12 days** to open WhatsApp on the primary phone so you never hit the 14‑day auto‑disconnect limit.
* Avoid frequently switching phones for the same WhatsApp number; this can trigger additional security checks and disconnects.
{% endhint %}

