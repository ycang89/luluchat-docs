# Connect your Channel

## What is Channel Connection?
Connecting your channel links your WhatsApp account (Personal or Business Cloud) to Luluchat. This allows you to manage conversations, run automations, and send broadcasts directly from the platform.

## When does it trigger?
- When you first open `Inbox` and no channel is connected.
- When your existing channel is disconnected or requires re-authentication.

## How to set it up (Step by Step)

### Step 1: Open Inbox
Click `Inbox` in the left menu. if your channel is not yet connected, you will automatically be directed to the **Connect your Channel** page.

📸 Screenshot placeholder:
> [Screenshot: Channel selection page showing WhatsApp Personal and WhatsApp Cloud options]

### Step 2: Choose your Channel Type
Select the type of WhatsApp account you want to connect:
- **WhatsApp Personal**: For standard WhatsApp or WhatsApp Business app accounts.
- **WhatsApp Cloud**: For accounts using the official WhatsApp Business API (WABA).

---

### Connecting WhatsApp Personal

#### Step 3a: Scan QR Code
Luluchat will generate a QR code. Open WhatsApp on your phone, go to **Linked Devices**, and scan the code shown on the screen.

📸 Screenshot placeholder:
> [Screenshot: WhatsApp Personal connection page with QR code]

#### Step 3b: Link with Phone Number (Alternative)
If you cannot scan the QR code, click **Link with Phone Number**. Enter your phone number to receive a pairing code, then enter that code in your WhatsApp app's "Link with Phone Number" section.

📸 Screenshot placeholder:
> [Screenshot: Pairing code entry for phone number linking]

---

### Connecting WhatsApp Cloud (WABA)

#### Step 3c: Authenticate with Facebook
Follow the on-screen prompts to log in to your Facebook Business account and authorize Luluchat.

#### Step 4c: Select Phone Number
Choose the specific phone number from your WABA account that you want to use with Luluchat.

#### Step 5c: Enter OTP/PIN
Enter the verification code or PIN provided during the WABA setup process to finalize the connection.

📸 Screenshot placeholder:
> [Screenshot: WhatsApp Cloud setup form showing phone selection and PIN fields]

---

### Step 6: Wait for Sync
Once connected, Luluchat will begin syncing your contacts and messages. You will see a "Syncing contacts..." status before the Inbox fully loads.

📸 Screenshot placeholder:
> [Screenshot: Inbox loading/syncing state]

**Note:**
- Make sure your mobile phone has a good internet connection.
- Make sure you have the latest WhatsApp installed on your phone.
- If you have a very large number of contacts, it may take a while to sync. Please wait for 15 minutes before you start using the app.
- After you have connected WhatsApp to Luluchat, you need to log in to your primary phone every 14 days to keep linked devices connected to your WhatsApp account.

## What happens after it triggers?
Once the status changes to `ready`, you can start receiving and sending messages. Your Message Flows and Broadcasts will now be able to fire for this channel.

## Important behavior to know
- **One Channel per Workspace**: Most plans allow one active channel connection at a time.
- **Stay Connected**: For WhatsApp Personal, ensure your phone remains connected to the internet to maintain the link.
- **Re-authentication**: If your account is logged out from the phone or the session expires, you will need to repeat the connection steps.
- **14-Day Login Requirement**: For WhatsApp Personal, you must log in to your primary phone (the one linked to your WhatsApp account) at least once every 14 days to keep the linked device connection active. If you don't log in within 14 days, the connection will be automatically disconnected.
- **Disconnection Notification**: If your channel becomes disconnected, Luluchat will automatically send a notification message to your registered WhatsApp number to alert you about the disconnection. This helps you quickly identify and resolve connection issues.
- **Large Contact Lists**: If you have a very large number of contacts (thousands), the initial sync may take up to 15 minutes. Wait for the sync to complete before using the app to ensure all contacts are properly loaded.

## Common issues & solutions
- **QR Code not loading**: Refresh the page to generate a new code.
- **Failed to register (WABA)**: Ensure your Facebook Business account has the correct permissions and that the phone number is not used by another WABA integration.
- **Channel disconnected**:
  - Check your registered WhatsApp number for a disconnection notification message from Luluchat.
  - Re-scan the QR code or check your phone's linked devices list.
  - If disconnected due to 14-day inactivity, log in to your primary phone's WhatsApp and reconnect the channel.
  - Ensure your phone has a stable internet connection.
- **Sync taking too long**:
  - If you have a large number of contacts, wait up to 15 minutes for the initial sync to complete.
  - Check your internet connection speed - a slow connection will delay the sync process.
- **Connection lost frequently**:
  - Ensure your phone maintains a stable internet connection.
  - Make sure you're using the latest version of WhatsApp.
  - Log in to your primary phone's WhatsApp at least once every 14 days to maintain the link.

## Best practice 💡
- **Use a Dedicated Device**: For WhatsApp Personal, use a stable phone dedicated to business use to avoid accidental disconnections.
- **Monitor Status**: Check the connection status in the Inbox header regularly to ensure your automations are active.
- **Keep WhatsApp Updated**: Always use the latest version of WhatsApp on your phone to ensure compatibility and security.
- **Maintain Internet Connection**: Ensure your phone has a stable internet connection during the connection process and while using Luluchat.
- **Set Reminders**: Set a reminder to log in to your primary phone's WhatsApp at least once every 14 days to prevent automatic disconnection.
- **Monitor Notifications**: Pay attention to disconnection notification messages sent to your registered WhatsApp number so you can quickly address connection issues.
