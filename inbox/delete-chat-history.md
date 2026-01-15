# Delete Chat History

## What is Delete Chat History?

Delete Chat History is a feature that allows you to permanently remove all conversation messages and data associated with a channel when you disconnect it. This is useful when you want to start fresh with a channel or remove sensitive data before disconnecting.

## When does it trigger?

* When you disconnect a channel and check the "Remove chat history" option.
* Only available during the channel disconnection process.
* This action is permanent and cannot be undone.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Access Channel Management

1. Go to `Inbox` in the left menu.
2. If you have an existing channel connected, look for the channel selector or channel management option in the header or sidebar.
3. Alternatively, you can access channel management from the channel connection page.

📸 Screenshot placeholder:
> [Screenshot: Inbox page showing channel selector or channel management option]
{% endstep %}

{% step %}
#### Open Channel List

1. On the channel management page, you'll see a list of all your existing channels.
2. Each channel card shows its status, phone number, and connection information.
3. Locate the channel you want to disconnect and delete chat history for.

📸 Screenshot placeholder:
> [Screenshot: Channel list page showing all channels with their status]
{% endstep %}

{% step %}
#### Click Disconnect Button

1. Find the channel you want to disconnect.
2. Click the **"Disconnect"** button (usually shown as a red/danger button) on the channel card.
3. A confirmation dialog will appear asking if you're sure you want to disconnect the channel.

📸 Screenshot placeholder:
> [Screenshot: Channel card showing Disconnect button]
{% endstep %}

{% step %}
#### Check "Remove chat history" Option

1. In the confirmation dialog, you'll see a checkbox labeled **"Remove chat history"**.
2. Check this box if you want to permanently delete all chat history for this channel.
3. If you leave it unchecked, the channel will be disconnected but all chat history will be preserved.

📸 Screenshot placeholder:
> [Screenshot: Disconnect confirmation dialog showing "Remove chat history" checkbox]
{% endstep %}

{% step %}
#### Confirm Disconnection

1. Review your decision carefully, as deleting chat history is permanent.
2. Click **"Yes, proceed"** to confirm the disconnection.
3. If you checked "Remove chat history", all messages and conversation data will be permanently deleted.
4. The channel will be disconnected and removed from your active channels list.

📸 Screenshot placeholder:
> [Screenshot: Confirmation dialog with checked "Remove chat history" and "Yes, proceed" button]
{% endstep %}
{% endstepper %}

## What happens after it triggers?

When you disconnect a channel with "Remove chat history" checked:

1. **All Messages Deleted**: All conversation messages, including text, media, files, and attachments, are permanently removed from the system.
2. **Conversation History Removed**: The entire conversation history for all contacts associated with this channel is deleted.
3. **Channel Disconnected**: The channel is disconnected from Luluchat and removed from your active channels list.
4. **Data Permanently Removed**: This action cannot be undone. Once deleted, the chat history cannot be recovered.
5. **Contacts Preserved**: Contact information (names, phone numbers, custom attributes) may still be preserved depending on your settings, but all conversation messages are deleted.

## Important behavior to know

* **Permanent Action**: Deleting chat history is permanent and cannot be undone. Make sure you have backups if you need to preserve any important conversations.
* **Only During Disconnect**: The option to delete chat history is only available when disconnecting a channel. You cannot delete chat history for an active, connected channel.
* **All Messages Removed**: This removes all messages for all contacts that were associated with the disconnected channel.
* **No Recovery**: Once chat history is deleted, it cannot be recovered. This includes messages, media files, and conversation threads.
* **Channel Status**: You can only disconnect channels that are in certain statuses (not pending, not instantiated, not already disconnecting or disconnected).
* **Separate from Channel Disconnect**: You can disconnect a channel without deleting chat history. The checkbox is optional.
* **Team Impact**: If multiple team members had access to conversations on this channel, the deleted history will be removed for everyone.

## Common issues & solutions

* **Checkbox not appearing**:
  * Ensure the channel is in a disconnectable status (not pending, instantiated, disconnecting, or already disconnected).
  * Refresh the channel management page.
  * Check that you have the necessary permissions to disconnect channels.

* **Chat history still visible after disconnect**:
  * If you disconnected without checking "Remove chat history", the history is preserved. You would need to disconnect again with the checkbox checked to delete it.
  * Note: Once a channel is disconnected, you may need to reconnect it first if you want to delete its history (though this is not recommended as a workflow).

* **Accidentally deleted chat history**:
  * Unfortunately, deleted chat history cannot be recovered. Always ensure you have backups of important conversations before deleting.
  * Consider exporting important conversations before disconnecting if you need to preserve them.

* **Want to delete history without disconnecting**:
  * Currently, chat history deletion is only available during channel disconnection. If you need to clean up history while keeping the channel connected, you may need to contact support for alternative solutions.

## Best practice 💡

* **Backup Important Data**: Before deleting chat history, export or backup any important conversations, especially those containing customer information, agreements, or critical business data.
* **Use with Caution**: Only delete chat history when you're certain you don't need the conversation data. Consider archiving or exporting important conversations first.
* **Team Communication**: If you're working in a team, communicate with your team members before deleting chat history, as it affects everyone's access to those conversations.
* **Regular Cleanup**: If you regularly disconnect and reconnect channels, consider whether you need to preserve history for compliance or business continuity purposes.
* **Compliance Considerations**: Be aware of any data retention requirements or regulations that may apply to your business before deleting chat history.

## Related Documentation

- [Connect your Channel](connect-channel.md) - Learn how to connect channels
- [How to Add a New Channel](connect-channel.md#how-to-add-a-new-channel) - Learn how to add additional channels
- [Inbox Overview](index.md) - Learn about the Inbox module
