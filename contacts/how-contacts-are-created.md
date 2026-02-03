# How Contacts Are Created

## Overview

In Luluchat, contacts are automatically created in your contact list when certain conditions are met. Understanding how contacts are created helps you manage your audience effectively and troubleshoot issues with contact synchronization.

## When Are Contacts Created?

Contacts are **automatically created** when:

1. **An incoming message is received** - This is the primary way contacts are created in Luluchat
2. **A form response is submitted** - When a customer submits a form, a contact may be created if one doesn't exist
3. **Manual import** - When you import contacts via CSV or other methods
4. **Integration triggers** - Some integrations may create contacts when specific events occur

{% hint style="info" %}
**Key Point**: Contacts are created when there's an **actual incoming message** from a customer, not just when a conversation is opened or initiated.
{% endhint %}

## The Contact Creation Process

### Automatic Creation from Incoming Messages

When a customer sends you a message on WhatsApp:

1. **Message Received**: Luluchat receives the incoming message through the WhatsApp Business API webhook
2. **Contact Lookup**: The system checks if a contact already exists for that WhatsApp number in your channel
3. **Contact Creation**: If no contact exists, a new contact is automatically created with:
   - WhatsApp contact ID (phone number)
   - Display name (from WhatsApp profile or phone number)
   - Channel association
   - Initial message timestamp
4. **Message Processing**: The incoming message is then processed and associated with the contact

### What Information Is Captured?

When a contact is automatically created from an incoming message, the following information is captured:

- **WhatsApp Contact ID**: The phone number in WhatsApp format
- **Display Name**: The contact's name from their WhatsApp profile (if available)
- **Channel**: The specific WhatsApp channel where the message was received
- **First Message**: The initial message that triggered the contact creation
- **Timestamp**: When the contact was first created and when they last conversed

## Important Behavior: Facebook Ads Leads

### Understanding the Facebook Ads Scenario

A common question from clients is: **"Why don't all my Facebook Ads leads appear in my contact list?"**

The answer is related to how contacts are created in Luluchat:

{% hint style="warning" %}
**Important**: Contacts are only created when a customer **sends an actual message**, not just when they click on an ad or open a conversation.
{% endhint %}

### What Happens with Facebook Ads?

When you run Facebook Ads that direct users to WhatsApp:

1. **User Clicks Ad**: A potential customer clicks on your Facebook ad
2. **Conversation Opens**: The WhatsApp conversation opens on their device
3. **Two Possible Outcomes**:
   - **Scenario A**: User sends a message → Contact is **created** ✅
   - **Scenario B**: User closes without sending → Contact is **NOT created** ❌

### Why This Happens

Luluchat creates contacts based on **incoming messages** received through the WhatsApp Business API. If a user:
- Clicks on your Facebook ad
- Opens the WhatsApp conversation
- But **doesn't send any message**

Then no incoming message is received by Luluchat, and therefore **no contact is created** in your contact list.

This is expected behavior because:
- Luluchat only receives webhook notifications when actual messages are sent
- Simply opening a conversation doesn't trigger a webhook event
- This ensures your contact list only contains people who have actively engaged with you

### Best Practices for Facebook Ads

To maximize contact creation from Facebook Ads:

1. **Clear Call-to-Action**: Encourage users to send a message in your ad copy
2. **Engaging Ad Copy**: Use compelling messaging that prompts users to respond
3. **Follow-Up**: If you have access to Facebook Lead Ads, you can manually import those leads
4. **Track Engagement**: Monitor which ads generate actual messages vs. just clicks

## Manual Contact Creation

You can also create contacts manually through:

- **Import/Export**: Bulk import contacts from CSV files
- **Manual Entry**: Add individual contacts through the Contacts interface
- **API Integration**: Create contacts programmatically via API

For more information, see [Import & Export](import-export.md).

## Troubleshooting

### Contact Not Appearing After Message

If you sent a message to a customer but they don't appear in your contact list:

1. **Check the Channel**: Ensure you're looking in the correct channel's contact list
2. **Verify Message Delivery**: Confirm the message was actually delivered
3. **Wait a Moment**: Contact creation happens asynchronously - wait a few seconds
4. **Check Filters**: Make sure no filters are hiding the contact in your view

### Facebook Ads Leads Not Syncing

If Facebook Ads leads aren't appearing in your contact list:

1. **Check for Messages**: Verify if the lead actually sent a message
2. **Review Ad Performance**: Check Facebook Ads Manager to see click-through rates vs. actual conversations
3. **Consider Manual Import**: If you're using Facebook Lead Ads, import those leads manually
4. **Understand the Difference**: Remember that ad clicks ≠ contacts. Only actual messages create contacts.

## Related Documentation

- [Contacts Overview](index.md) - Learn about managing your contact database
- [Import & Export](import-export.md) - How to bulk import contacts
- [Bulk Actions](bulk-actions.md) - Manage multiple contacts at once
