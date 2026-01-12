# Broadcasts

## What is Broadcasts?
Broadcasts allow you to send a message flow to a large group of contacts at once. You can send these messages immediately or schedule them for a specific date and time, helping you engage your audience with announcements, updates, or promotions.

## When does it trigger?
- When a broadcast is sent immediately after creation.
- At the scheduled date and time if scheduling is enabled.
- Only during the configured "Broadcast Sending Hours" set in your workspace settings.

## How to set it up (Step by Step)

### Step 1: Open Broadcasts
Click `Broadcasts` in the left menu to view your broadcast list.

📸 Screenshot placeholder:
> [Screenshot: Broadcasts list view with 'Create Broadcast' button]

### Step 2: Create a new broadcast
Click the `Create Broadcast` button. You will be guided through a 3-step process.

📸 Screenshot placeholder:
> [Screenshot: Create Broadcast page showing the three configuration sections]

### Step 3: Fill up broadcast details
- **Broadcast Name**: Enter an internal name for your reference (e.g., "Monthly Newsletter").
- **Message Flow**: Choose the message flow you want to deliver. Only activated flows are listed.
- **Internal Notes**: (Optional) Add notes for your team to provide context about this broadcast.

📸 Screenshot placeholder:
> [Screenshot: Section 1 - Broadcast details with name and flow selection]

### Step 4: Define recipients
Choose who will receive the broadcast using one or more of these conditions:
- **Tags**: Include or exclude contacts based on their tags.
- **Manual Selection**: Pick specific contacts from your directory.
- **Inbox List**: Include all contacts from a specific inbox tab.
- **File Upload**: Upload a CSV file of phone numbers (must exist in your Contacts first).
- **Assignee**: Target contacts assigned to specific team members.

📸 Screenshot placeholder:
> [Screenshot: Section 2 - Recipient conditions showing tags, manual selection, and upload options]

### Step 5: Configure advanced settings
- **Scheduling**: Toggle "Yes" to pick a future date and time for the broadcast.
- **Archive Chat**: Toggle "Yes" to automatically move these conversations to the Archived list in your Inbox after the broadcast is sent.

📸 Screenshot placeholder:
> [Screenshot: Section 3 - Advanced settings with scheduling and archive toggles]

### Step 6: Review and save
Click `Create` to finalize. If not scheduled, it will begin sending (respecting your daily limits and hours).

## What happens after it triggers?
The system begins delivering the message flow to each recipient. You can track progress from the Broadcasts list, seeing statistics like how many messages are remaining.

## Important behavior to know
- **Daily Limits and Capacity**: Your daily broadcast capacity is determined by your settings in [Settings: Broadcast](./settings/broadcast.md). It depends on your **Broadcast Message Interval**, **Broadcast Start Time**, and **Broadcast End Time**.
- **Sending Hours**: Broadcasts only send during your configured sending window. If you schedule a broadcast outside these hours, the system will queue it and begin sending at the next start time.
- **Channel Connection**: Your channel must be connected (`ready` status) for broadcasts to send.
- **Pause/Resume**: You can pause an active broadcast at any time from the "More" menu in the list view.

## Common issues & solutions
- **Broadcast not sending**: Check if your channel is connected and if you are within your "Broadcast Sending Hours."
- **Daily limit reached**: If you exceed your daily quota, the remaining messages will wait until your quota resets.
- **CSV upload failed**: Ensure the phone numbers in your file already exist in your Contacts directory.

## Best practice 💡
- **Test first**: Send the message flow to a test contact before broadcasting to a large group.
- **Timing matters**: Schedule broadcasts during your audience's active hours for better engagement.
- **Use tags**: Segment your audience with tags to ensure your message is relevant to the recipients.
