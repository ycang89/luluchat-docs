# How to Migrate a WhatsApp Business API Account

## What is WABA Account Migration?

Migrating a WhatsApp Business API (WABA) account means transferring your WABA phone number and business account from one Meta Business Account to another, or from one WhatsApp Business API provider to another (like moving to Luluchat). This process allows you to maintain your phone number, business verification status, and messaging history while switching platforms or business accounts.

## When Do You Need to Migrate?

You may need to migrate your WABA account in these scenarios:

* **Switching to Luluchat**: Moving from another WhatsApp Business API provider to Luluchat
* **Changing Meta Business Account**: Transferring your WABA to a different Meta Business Account
* **Consolidating Accounts**: Merging multiple WABA accounts into one
* **Changing Business Structure**: Reorganizing your business setup in Meta Business Manager

## Important Considerations Before Migration

{% hint style="warning" %}
**Critical Information to Know Before Starting**

* **Phone Number**: Your phone number can only be associated with one WABA account at a time. You must disconnect it from the old account before connecting to the new one.
* **Business Verification**: If your business is verified, you'll need to re-verify after migration. However, the verification process may be faster if you've been verified before.
* **Message Templates**: All approved message templates need to be recreated in the new account. Template approvals cannot be transferred.
* **Messaging History**: Message history and conversation data are tied to the WABA account and cannot be directly transferred. You may need to export important data before migration.
* **Service Window**: The 24-hour service window is reset after migration. You'll need to re-establish conversations with contacts.
* **Messaging Limits**: Your messaging tier and limits may reset after migration, depending on your new account setup.
* **Downtime**: There will be a brief period where your WABA account is disconnected and cannot send messages.
{% endhint %}

## Migration Process Overview

The migration process involves these main steps:

1. **Prepare Your New Account**: Set up your new Meta Business Account and WABA in Luluchat
2. **Export Important Data**: Save any critical information from your old account
3. **Disconnect from Old Account**: Remove your phone number from the old WABA account
4. **Connect to New Account**: Link your phone number to the new WABA account in Luluchat
5. **Recreate Templates**: Recreate and resubmit your message templates
6. **Re-verify Business** (if applicable): Complete business verification if needed
7. **Test and Verify**: Ensure everything works correctly

## Step-by-Step Migration Guide

### Step 1: Prepare Your New WABA Account in Luluchat

{% stepper %}
{% step %}
#### Create or Access Your Meta Business Account

1. Go to [Meta Business Manager](https://business.facebook.com/)
2. Create a new Meta Business Account (if you don't have one) or access your existing one
3. Ensure you have admin access to the business account

📸 Screenshot placeholder:
> [Screenshot: Meta Business Manager dashboard]
{% endstep %}

{% step %}
#### Set Up WhatsApp Business Account

1. In Meta Business Manager, go to **Business Settings** > **Accounts** > **WhatsApp Accounts**
2. Click **Add** to create a new WhatsApp Business Account
3. Follow the setup wizard to create your WABA

📸 Screenshot placeholder:
> [Screenshot: Creating WhatsApp Business Account in Meta Business Manager]
{% endstep %}

{% step %}
#### Get Your WABA Credentials

You'll need these credentials to connect in Luluchat:
* **Phone Number ID**: Found in your WABA settings
* **Business Account ID**: Your Meta Business Account ID
* **Permanent Access Token**: Generated in Meta Business Manager

📸 Screenshot placeholder:
> [Screenshot: WABA settings showing Phone Number ID and Business Account ID]
{% endstep %}
{% endstepper %}

### Step 2: Export Important Data from Old Account

Before disconnecting, export any critical information:

{% stepper %}
{% step %}
#### Export Message Templates

1. In your old WABA provider, go to Message Templates
2. Document all approved templates (name, category, content, buttons, etc.)
3. Take screenshots or export template details
4. Note which templates are currently in use

📸 Screenshot placeholder:
> [Screenshot: Message Templates list in old account]
{% endstep %}

{% step %}
#### Export Contact Data

1. Export your contact list if possible
2. Note any important custom attributes or tags
3. Document any active conversations or important message history

📸 Screenshot placeholder:
> [Screenshot: Contact export options]
{% endstep %}

{% step %}
#### Document Business Verification Status

1. Note your current verification status (if verified)
2. Save any verification documents or certificates
3. Document your business information used for verification

📸 Screenshot placeholder:
> [Screenshot: Business verification status page]
{% endstep %}
{% endstepper %}

### Step 3: Disconnect from Old Account

{% stepper %}
{% step %}
#### Remove Phone Number from Old WABA

1. Log into your old WhatsApp Business API provider
2. Navigate to your WABA account settings
3. Find the option to remove or disconnect your phone number
4. Follow the disconnection process

{% hint style="warning" %}
**Important**: Only disconnect after you have your new account ready. There will be downtime between disconnection and reconnection.
{% endhint %}

📸 Screenshot placeholder:
> [Screenshot: Phone number disconnection option in old provider]
{% endstep %}

{% step %}
#### Verify Disconnection

1. Confirm that your phone number is no longer associated with the old WABA account
2. Wait a few minutes to ensure the disconnection is complete
3. You may receive a notification confirming the disconnection

📸 Screenshot placeholder:
> [Screenshot: Disconnection confirmation message]
{% endstep %}
{% endstepper %}

### Step 4: Connect to Luluchat

{% stepper %}
{% step %}
#### Open Channel Connection in Luluchat

1. Go to **Inbox** in Luluchat
2. Click **Connect your Channel** (or navigate to channel settings if already connected)
3. Select **WhatsApp Cloud** (WABA)

📸 Screenshot placeholder:
> [Screenshot: Channel connection page with WhatsApp Cloud option]
{% endstep %}

{% step %}
#### Enter WABA Credentials

1. Enter your **Phone Number ID** from Meta Business Manager
2. Enter your **Business Account ID**
3. Enter your **Permanent Access Token**
4. Click **Connect**

{% hint style="info" %}
**Where to Find Credentials**:
- **Phone Number ID**: Meta Business Manager > WhatsApp Accounts > Your Account > Phone Numbers
- **Business Account ID**: Meta Business Manager > Business Settings > Accounts > WhatsApp Accounts
- **Permanent Access Token**: Meta Business Manager > System Users > Generate Token (requires appropriate permissions)

For detailed instructions, see [Connect Your Channel](../inbox/connect-channel.md) and [Integration Settings](../settings/account/integration.md).
{% endhint %}

📸 Screenshot placeholder:
> [Screenshot: WABA connection form with credential fields]
{% endstep %}

{% step %}
#### Verify Connection

1. Wait for Luluchat to verify and connect your WABA account
2. You should see a confirmation message when the connection is successful
3. Your phone number should now appear as connected in Luluchat

📸 Screenshot placeholder:
> [Screenshot: Successful WABA connection confirmation]
{% endstep %}
{% endstepper %}

### Step 5: Recreate Message Templates

{% stepper %}
{% step %}
#### Access Message Templates

1. Go to **Message Templates** in Luluchat
2. Click **Create Template** or **Sync Templates** (if available)

📸 Screenshot placeholder:
> [Screenshot: Message Templates page in Luluchat]
{% endstep %}

{% step %}
#### Recreate Your Templates

1. For each template from your old account:
   - Click **Create Template**
   - Enter the template name, category, and content
   - Add buttons or interactive elements if applicable
   - Submit for approval

2. **Note**: Templates must be approved by WhatsApp before you can use them. This can take minutes to 24 hours.

📸 Screenshot placeholder:
> [Screenshot: Creating a new message template]
{% endstep %}

{% step %}
#### Update Your Message Flows

1. Go to **Automations** > **Message Flows**
2. Update any flows that reference old templates
3. Replace old template references with your newly created templates

📸 Screenshot placeholder:
> [Screenshot: Message Flow editor showing template selection]
{% endstep %}
{% endstepper %}

### Step 6: Re-verify Your Business (If Applicable)

If your business was verified before, you may need to re-verify:

{% stepper %}
{% step %}
#### Check Verification Status

1. In Meta Business Manager, check your business verification status
2. If not verified, you'll see an option to start verification

📸 Screenshot placeholder:
> [Screenshot: Business verification status in Meta Business Manager]
{% endstep %}

{% step %}
#### Complete Verification Process

1. Follow the business verification process in Meta Business Manager
2. Submit required documents and information
3. Wait for approval (this can take several days to weeks)

For detailed information, see [Business Verification](./business-verification.md).

📸 Screenshot placeholder:
> [Screenshot: Business verification application form]
{% endstep %}
{% endstepper %}

### Step 7: Test and Verify

{% stepper %}
{% step %}
#### Test Message Sending

1. Send a test message to yourself or a test contact
2. Verify that messages are delivered correctly
3. Test template messages if applicable

📸 Screenshot placeholder:
> [Screenshot: Test message in Inbox]
{% endstep %}

{% step %}
#### Verify Message Flows

1. Test your automated message flows
2. Ensure all flows are working correctly with new templates
3. Check that triggers and actions function as expected

📸 Screenshot placeholder:
> [Screenshot: Testing a message flow]
{% endstep %}

{% step %}
#### Check Broadcasts

1. Review your broadcast settings
2. Test a small broadcast to ensure it works
3. Verify that broadcast limits and settings are correct

📸 Screenshot placeholder:
> [Screenshot: Broadcast test results]
{% endstep %}
{% endstepper %}

## Important Behavior to Know

* **Phone Number Transfer**: Your phone number can only be connected to one WABA account at a time. The disconnection from the old account must complete before connecting to the new one.
* **Template Approval**: All message templates must be recreated and re-approved. Template approvals cannot be transferred between accounts.
* **Business Verification**: If you were verified before, you may need to re-verify. However, the process may be faster if you've been verified previously.
* **Service Window Reset**: The 24-hour service window resets after migration. You'll need to re-establish conversations with contacts or use approved templates.
* **Messaging Limits**: Your messaging tier and limits may reset. You may start at a lower tier and need to build up your quality rating again.
* **Message History**: Historical messages and conversations cannot be transferred. Only new messages after migration will appear in Luluchat.
* **Downtime**: Expect a brief downtime (typically 15-30 minutes) during the migration process when messages cannot be sent.
* **Contact Sync**: Contacts will need to be re-imported or will sync automatically as they message you after migration.

## Common Issues & Solutions

* **Phone number already in use**: Ensure you've completely disconnected from the old account. Wait a few minutes and try again.
* **Connection fails**: Verify all credentials are correct (Phone Number ID, Business Account ID, Access Token). Check that your access token has the necessary permissions.
* **Templates not approved**: Template approval can take time. Check the template status in Meta Business Manager and wait for approval before using.
* **Messages not sending**: Verify your channel is connected and ready. Check that you're within the service window or using approved templates.
* **Business verification pending**: Business verification can take time. Continue using your account while verification is in progress (with appropriate messaging limits).
* **Contacts not syncing**: Contacts will sync automatically as they message you. You can also import contacts manually through the Contacts page.

## Best Practice 💡

* **Plan Ahead**: Schedule migration during low-traffic periods to minimize disruption
* **Document Everything**: Keep detailed records of templates, settings, and configurations from your old account
* **Test Thoroughly**: Test all critical functions (messaging, flows, broadcasts) after migration
* **Communicate with Customers**: Inform customers about potential brief downtime if necessary
* **Monitor Closely**: Watch for any issues in the first few days after migration
* **Backup Data**: Export and backup any important data before starting migration
* **Coordinate with Support**: If you encounter issues, contact Luluchat support or Meta support as needed

## Related Documentation

- [Connect Your Channel](../inbox/connect-channel.md) - Detailed guide on connecting WABA in Luluchat
- [Integration Settings](../settings/account/integration.md) - How to manage WABA credentials
- [Message Templates](../message-templates.md) - How to create and manage message templates
- [Business Verification](./business-verification.md) - Complete guide on business verification
- [Service Window](./service-window.md) - Understanding the 24-hour messaging window
- [Messaging Limits & Quality](./messaging-limits-quality.md) - Information about messaging tiers and limits
