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

## What happens after it triggers?
Once the status changes to `ready`, you can start receiving and sending messages. Your Message Flows and Broadcasts will now be able to fire for this channel.

## Important behavior to know
- **One Channel per Workspace**: Most plans allow one active channel connection at a time.
- **Stay Connected**: For WhatsApp Personal, ensure your phone remains connected to the internet to maintain the link.
- **Re-authentication**: If your account is logged out from the phone or the session expires, you will need to repeat the connection steps.

## Common issues & solutions
- **QR Code not loading**: Refresh the page to generate a new code.
- **Failed to register (WABA)**: Ensure your Facebook Business account has the correct permissions and that the phone number is not used by another WABA integration.
- **Channel disconnected**: Re-scan the QR code or check your phone's linked devices list.

## Best practice 💡
- **Use a Dedicated Device**: For WhatsApp Personal, use a stable phone dedicated to business use to avoid accidental disconnections.
- **Monitor Status**: Check the connection status in the Inbox header regularly to ensure your automations are active.
