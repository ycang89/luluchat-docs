# Broadcasts

## What is Broadcasts?

Broadcasts allow you to send a message flow to a large group of contacts at once. You can send these messages immediately or schedule them for a specific date and time, helping you engage your audience with announcements, updates, or promotions.

## When does it trigger?

* When a broadcast is sent immediately after creation.
* At the scheduled date and time if scheduling is enabled.
* Only during the configured "Broadcast Sending Hours" set in your workspace settings.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Open Broadcasts

Click `Broadcasts` in the left menu to view your broadcast list.

📸 Screenshot placeholder:

> \[Screenshot: Broadcasts list view with 'Create Broadcast' button]
{% endstep %}

{% step %}
#### Create a new broadcast

Click the `Create Broadcast` button. You will be guided through a 3-step process.

📸 Screenshot placeholder:

> \[Screenshot: Create Broadcast page showing the three configuration sections]
{% endstep %}

{% step %}
#### Fill up broadcast details

* Broadcast Name: Enter an internal name for your reference (e.g., "Monthly Newsletter").
* Message Flow: Choose the message flow you want to deliver. Only activated flows are listed.
* Internal Notes: (Optional) Add notes for your team to provide context about this broadcast.

📸 Screenshot placeholder:

> \[Screenshot: Section 1 - Broadcast details with name and flow selection]
{% endstep %}

{% step %}
#### Define recipients

Choose who will receive the broadcast using one or more of these conditions:

* Tags: Include or exclude contacts based on their tags.
* Manual Selection: Pick specific contacts from your directory.
* Inbox List: Include all contacts from a specific inbox tab.
* File Upload: Upload a CSV file of phone numbers (must exist in your Contacts first).
* Assignee: Target contacts assigned to specific team members.

{% hint style="warning" %}
Important: Only contacts that meet both of these criteria will receive broadcasts:

* Imported Contacts: Contacts must be imported or added through the Contacts page. Contacts who have only messaged you but haven't been added to your Contacts directory will not receive broadcasts.
* Not Opted Out: Contacts must not have opted out. Opted-out contacts are automatically excluded from all broadcasts.
{% endhint %}

📸 Screenshot placeholder:

> \[Screenshot: Section 2 - Recipient conditions showing tags, manual selection, and upload options]
{% endstep %}

{% step %}
#### Configure advanced settings

* Scheduling: Toggle "Yes" to pick a future date and time for the broadcast.
* Archive Chat: Toggle "Yes" to automatically move these conversations to the Archived list in your Inbox after the broadcast is sent.

📸 Screenshot placeholder:

> \[Screenshot: Section 3 - Advanced settings with scheduling and archive toggles]
{% endstep %}

{% step %}
#### Review and save

Click `Create` to finalize. If not scheduled, it will begin sending (respecting your daily limits and hours).
{% endstep %}
{% endstepper %}

## What happens after it triggers?

The system begins delivering the message flow to each recipient. You can track progress from the Broadcasts list, seeing statistics like how many messages are remaining. You can also view detailed message status in the **Broadcast Message Queue** section on the broadcast details page.

## Broadcast Message Queue

The Broadcast Message Queue provides a detailed view of each message's status in your broadcast. You can access it by opening any broadcast from the Broadcasts list and scrolling to the "Broadcast Message Queue" section at the bottom of the page.

### Message Statuses

The queue organizes messages into six status categories, accessible via tabs:

| Status                      | Description                                                                                                                                                                                                         | Information Shown                                                                                                                                              | Special Actions                                                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| **Delivered (Sent)**        | Messages that have been successfully sent to recipients                                                                                                                                                             | <p>• WhatsApp number<br>• Contact name<br>• Processed timestamp (when the message was sent)</p>                                                                | —                                                                                                                                           |
| **Read**                    | Messages that have been read by recipients                                                                                                                                                                          | <p>• WhatsApp number<br>• Contact name<br>• Processed timestamp (when the message was sent)<br>• Link to open the conversation in Inbox</p>                    | Click inbox link to view conversation                                                                                                       |
| **Replied**                 | Messages where recipients have replied to your broadcast                                                                                                                                                            | <p>• WhatsApp number<br>• Contact name<br>• Processed timestamp (when the message was sent)<br>• Link to open the conversation in Inbox</p>                    | Click inbox link to view conversation                                                                                                       |
| **Replied to Given Option** | Messages where recipients have interacted with buttons or quick reply options in your message flow. For example, if your message includes interactive buttons, this tab shows contacts who clicked on those buttons | <p>• WhatsApp number<br>• Contact name<br>• Processed timestamp (when the message was sent)<br>• Link to open the conversation in Inbox</p>                    | Click inbox link to view conversation                                                                                                       |
| **Failed**                  | Messages that failed to send                                                                                                                                                                                        | <p>• WhatsApp number<br>• Contact name<br>• Remarks (error details explaining why the message failed)<br>• Processed timestamp (when the failure occurred)</p> | Select multiple failed messages and use "Resend to Selected" button to retry sending them, or use "Resend All" to retry all failed messages |
| **Remaining**               | Messages that are still in the queue waiting to be sent                                                                                                                                                             | <p>• WhatsApp number<br>• Contact name</p>                                                                                                                     | These messages will be sent according to your broadcast settings (sending hours, daily limits, and message interval)                        |

📸 Screenshot placeholder:

> \[Screenshot: Broadcast Message Queue showing different status tabs]

### Queue Management Actions

#### Pause/Resume Broadcast

* **Pause**: Click the `Pause` button in the queue toolbar to temporarily stop sending messages. The broadcast will pause, and remaining messages will stay in the queue.
* **Resume**: If a broadcast is paused, click the `Resume` button to continue sending messages from where it left off.

📸 Screenshot placeholder:

> \[Screenshot: Broadcast Message Queue toolbar showing Pause/Resume button]

#### Resend Failed Messages

For messages in the "Failed" tab:

* **Resend All**: Click `Resend All` to retry sending all failed messages.
* **Resend to Selected**: Select specific failed messages using the checkboxes, then click `Resend to Selected` to retry only those messages.

📸 Screenshot placeholder:

> \[Screenshot: Failed tab with selected messages and Resend to Selected button]

#### Export Queue Data

Click the `Export` button to download a CSV file of the current tab's data. This is useful for analyzing broadcast performance or creating reports.

📸 Screenshot placeholder:

> \[Screenshot: Export button in queue toolbar]

### How to use the Queue (Step by Step)

#### Step 1: Open Broadcast Details

From the Broadcasts list, click on any broadcast to open its details page.

📸 Screenshot placeholder:

> \[Screenshot: Broadcasts list with a broadcast selected]

#### Step 2: Navigate to Message Queue

Scroll down to the "Broadcast Message Queue" section at the bottom of the broadcast details page.

📸 Screenshot placeholder:

> \[Screenshot: Broadcast details page showing Message Queue section]

#### Step 3: View Status by Tab

Click on any status tab (Delivered, Read, Replied, Replied to Given Option, Failed, Remaining) to view messages in that status.

📸 Screenshot placeholder:

> \[Screenshot: Message Queue tabs showing different statuses]

#### Step 4: Search and Filter

Use the search box to find specific contacts by WhatsApp number or contact name within each status tab.

📸 Screenshot placeholder:

> \[Screenshot: Search box in Message Queue]

#### Step 5: Manage Queue (if needed)

* **Pause/Resume**: Use the Pause/Resume button to control broadcast sending.
* **Resend Failed**: If there are failed messages, select them and click "Resend to Selected" or "Resend All".
* **Export**: Click Export to download the queue data for analysis.

📸 Screenshot placeholder:

> \[Screenshot: Queue management actions]

{% hint style="info" %}
**Important behavior to know**

* **Contact Eligibility**: Only contacts that are:
  * **Imported to Contacts**: Contacts must be added or imported through the Contacts page. Contacts who have only messaged you but haven't been added to your Contacts directory will not receive broadcasts.
  * **Not Opted Out**: Contacts who have opted out are automatically excluded from all broadcasts, regardless of your selection criteria.
* **Daily Limits and Capacity**: Your daily broadcast capacity is determined by your settings in [Settings: Broadcast](settings/broadcast.md). It depends on your **Broadcast Message Interval**, **Broadcast Start Time**, and **Broadcast End Time**.
* **Sending Hours**: Broadcasts only send during your configured sending window. If you schedule a broadcast outside these hours, the system will queue it and begin sending at the next start time.
* **Channel Connection**: Your channel must be connected (`ready` status) for broadcasts to send.
* **Pause/Resume**: You can pause an active broadcast at any time from the "More" menu in the list view or from the Broadcast Message Queue toolbar. When you resume, sending continues from where it left off.
* **Message Status Tracking**: Message statuses (Delivered, Read, Replied, etc.) are automatically updated as recipients interact with your messages. The queue provides real-time visibility into broadcast performance.
* **Failed Messages**: Failed messages remain in the "Failed" tab until you manually resend them. Common failure reasons include invalid phone numbers, opted-out contacts, or temporary delivery issues.
* **Replied to Given Option**: This status specifically tracks interactions with interactive elements (buttons, quick replies) in your message flow, not just any reply. It helps you identify contacts who engaged with specific call-to-action options.
* **Remaining Queue**: Messages in the "Remaining" tab will be sent automatically according to your broadcast settings. You cannot manually send individual messages from this queue, but you can pause/resume the entire broadcast.
{% endhint %}

## Common issues & solutions

* **Broadcast not sending**: Check if your channel is connected and if you are within your "Broadcast Sending Hours."
* **Daily limit reached**: If you exceed your daily quota, the remaining messages will wait until your quota resets. Check the "Remaining" tab in the Message Queue to see queued messages.
* **CSV upload failed**: Ensure the phone numbers in your file already exist in your Contacts directory.
* **Contacts not receiving broadcasts**:
  * Verify that contacts are imported or added through the Contacts page. Contacts who have only messaged you but haven't been added to Contacts will not receive broadcasts.
  * Check if contacts have opted out. Opted-out contacts are automatically excluded from broadcasts.
  * Ensure contacts match your selection criteria (tags, assignee, etc.).
* **Fewer recipients than expected**:
  * Some contacts may have opted out and are automatically excluded.
  * Contacts who haven't been imported to your Contacts directory are excluded.
  * Check that your selection criteria (tags, assignee, etc.) match the contacts you want to reach.
* **Many messages in "Failed" tab**:
  * Review the "Remarks" column to understand why messages failed. Common reasons include invalid phone numbers, opted-out contacts, or temporary delivery issues.
  * Use "Resend to Selected" or "Resend All" to retry failed messages after addressing the underlying issues.
  * Check your channel connection status - a disconnected channel will cause all messages to fail.
* **Messages stuck in "Remaining" tab**:
  * Check if the broadcast is paused. If paused, click "Resume" to continue sending.
  * Verify you're within your "Broadcast Sending Hours" - messages only send during configured hours.
  * Check if you've reached your daily message limit - remaining messages will queue until the limit resets.
* **Can't see "Replied to Given Option" messages**:
  * This tab only shows contacts who interacted with interactive elements (buttons, quick replies) in your message flow.
  * If your message flow doesn't include interactive elements, this tab will be empty.
  * Regular text replies appear in the "Replied" tab, not "Replied to Given Option".

{% hint style="success" %}
**Best practice**

* **Import Contacts First**: Before creating a broadcast, ensure all intended recipients are imported or added through the Contacts page. Contacts who have only messaged you but aren't in your Contacts directory won't receive broadcasts.
* **Check Opt-Out Status**: Review your contact list to identify opted-out contacts before creating broadcasts to avoid confusion about delivery.
* **Test first**: Send the message flow to a test contact before broadcasting to a large group.
* **Timing matters**: Schedule broadcasts during your audience's active hours for better engagement.
* **Use tags**: Segment your audience with tags to ensure your message is relevant to the recipients.
* **Monitor the Queue**: Regularly check the Broadcast Message Queue to track delivery status, identify failed messages, and monitor engagement (read, reply rates).
* **Review Failed Messages**: Periodically review the "Failed" tab to identify patterns (e.g., invalid numbers, opt-outs) and clean up your contact list.
* **Use Interactive Elements**: Include buttons or quick replies in your message flow to track engagement via the "Replied to Given Option" tab and improve response rates.
* **Export for Analysis**: Use the Export feature to download queue data and analyze broadcast performance over time.
* **Resume Strategically**: If you pause a broadcast, resume it during your configured sending hours to ensure messages are delivered at optimal times.
{% endhint %}
