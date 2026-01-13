# Remind Me

## What is Remind Me?
Remind Me is a feature that lets you set reminders for conversations in your Inbox. You can schedule reminders to notify yourself or team members at a specific date and time. Reminders appear in the notification bell icon in the header bar and can send notifications via the web interface or mobile push notifications (for Pro plan subscribers).

## When to use it?
- **Follow-up Tasks**: Set reminders to follow up with customers after a specific time period.
- **Scheduled Check-ins**: Remind yourself to check on conversations that need attention later.
- **Team Coordination**: Notify team members about conversations that need their attention at a specific time.
- **Task Management**: Keep track of important conversations that require action at a future date.

## How to create a reminder (Step by Step)

<steps>
<step>
**Open a Conversation**

In your Inbox, click on any conversation to open it.

📸 Screenshot placeholder:
> [Screenshot: Inbox with a conversation selected and opened]
</step>

<step>
**Access Remind Me**

Click the three-dot menu (⋮) or the "Remind me" button in the conversation header bar.

📸 Screenshot placeholder:
> [Screenshot: Conversation header showing three-dot menu with "Remind me" option]
</step>

<step>
**Fill in Reminder Details**

In the "Create a Reminder" modal, configure your reminder:

- **Notify to Team User** (Required): Select one or more team members who should receive the reminder notification. You can select multiple users.
- **Title** (Required): Enter a title for the reminder (max 100 characters). By default, it's pre-filled with "Follow up with [Contact Name]".
- **Date** (Required): Select the date when you want to be reminded.
- **Time** (Required): Select the time when you want to be reminded. Time is set in 15-minute intervals (e.g., 09:00, 09:15, 09:30).
- **Description** (Optional): Add additional notes or context about the reminder.

📸 Screenshot placeholder:
> [Screenshot: Create a Reminder modal with all fields filled in]
</step>

<step>
**Save the Reminder**

Click the submit button to create the reminder. You'll see a success message confirming the reminder was created with the date and time.

📸 Screenshot placeholder:
> [Screenshot: Success message showing reminder created confirmation]
</step>
</steps>

## How to view and manage reminders (Step by Step)

<steps>
<step>
**Open Notifications**

Click the bell icon (🔔) in the header bar to open the notifications panel.

📸 Screenshot placeholder:
> [Screenshot: Header bar with bell icon highlighted]
</step>

<step>
**Switch to Reminders Tab**

In the notifications panel, click the **"Reminders"** tab to view your reminders.

📸 Screenshot placeholder:
> [Screenshot: Notifications panel showing Notifications and Reminders tabs]
</step>

<step>
**Filter Reminders**

Use the segmented control to filter reminders by status:
- **Upcoming**: Reminders scheduled for future dates
- **Overdue**: Reminders that have passed their scheduled time but haven't been marked as done
- **Done**: Reminders that have been completed

📸 Screenshot placeholder:
> [Screenshot: Reminders tab showing Upcoming, Overdue, and Done filter options]
</step>

<step>
**Search Reminders (Optional)**

Use the search box to find specific reminders by title or description.

📸 Screenshot placeholder:
> [Screenshot: Search box in Reminders tab]
</step>

<step>
**Manage Reminders**

For each reminder, you can:
- **View Details**: Click on a reminder to see its full details.
- **Edit**: Click the edit icon to modify the reminder (only for reminders you created).
- **Mark as Done**: Click to mark the reminder as completed (moves it to "Done" tab).
- **Delete**: Click the delete icon to remove the reminder permanently.
- **Go to Chat**: Click "Go to Chat" to open the conversation associated with the reminder.

📸 Screenshot placeholder:
> [Screenshot: Reminder list showing action buttons for edit, mark as done, and delete]
</step>
</steps>

## What happens after you create a reminder?
- **Reminder Created**: The reminder is saved and appears in your Reminders list.
- **Notification Sent**: At the scheduled date and time, notifications are sent to the selected team members:
  - **Web Notification**: All users receive notifications in the web interface (bell icon badge).
  - **Mobile Push Notification**: Pro plan subscribers also receive push notifications on the WhatsApp mobile app.
- **Reminder Appears**: The reminder appears in the Reminders tab under "Upcoming" until its scheduled time.
- **Status Updates**: After the scheduled time passes, the reminder moves to "Overdue" if not marked as done.

{% hint style="info" %}
**Important behavior to know**

- **Pro Plan Feature**: Mobile push notifications (WhatsApp app notifications) are only available for Pro plan subscribers. All users receive web notifications.
- **Time Intervals**: Time selection is limited to 15-minute intervals (e.g., 09:00, 09:15, 09:30, 09:45).
- **Default Values**: When creating a reminder, the title is pre-filled with "Follow up with [Contact Name]", the date defaults to tomorrow, and the time defaults to 09:00.
- **Edit Permissions**: Only the user who created a reminder can edit it. Other team members can view but not modify reminders created by others.
- **Multiple Notifications**: You can select multiple team members to notify. All selected members will receive the notification at the scheduled time.
- **Reminder Link**: Each reminder is linked to the specific conversation where it was created. You can click "Go to Chat" to return to that conversation.
- **Automatic Status**: Reminders automatically move from "Upcoming" to "Overdue" when their scheduled time passes (if not marked as done).
{% endhint %}

## Common issues & solutions
- **Can't see Remind Me option**:
  - The "Remind me" option is only available for WhatsApp Personal channels, not WhatsApp Cloud (WABA) channels.
  - Ensure you're viewing a conversation, not just the inbox list.

- **Reminder not appearing**:
  - Check that you're looking in the correct tab (Upcoming, Overdue, or Done).
  - Verify the reminder was successfully created (check for success message).
  - Try refreshing the page.

- **Not receiving notifications**:
  - Check that you were selected as a team user in the reminder.
  - Verify the reminder's scheduled time has passed.
  - For mobile push notifications, ensure you're on a Pro plan and have the WhatsApp app installed.
  - Check your browser's notification permissions for web notifications.

- **Can't edit reminder**:
  - Only the user who created the reminder can edit it. If you didn't create it, you can only view or delete it.
  - Completed reminders (in "Done" tab) cannot be edited.

- **Reminder in wrong tab**:
  - "Upcoming" shows reminders scheduled for future dates.
  - "Overdue" shows reminders whose scheduled time has passed but aren't marked as done.
  - "Done" shows reminders that have been marked as completed.

## Best practice 💡
- **Clear Titles**: Use descriptive titles that clearly indicate what action is needed (e.g., "Follow up on pricing quote", "Check order status").
- **Set Realistic Times**: Choose reminder times that align with your working hours and availability.
- **Use Descriptions**: Add context in the description field to help you remember why you set the reminder.
- **Team Coordination**: Use reminders to notify team members about conversations that need their attention.
- **Regular Review**: Check your "Overdue" tab regularly to ensure no important reminders are missed.
- **Mark as Done**: Mark reminders as done once you've completed the task to keep your list organized.

## Related Documentation
- [Inbox Overview](./index.md) - Learn about the Inbox module
- [Close Conversation](./close-conversation.md) - Learn how to close conversations
