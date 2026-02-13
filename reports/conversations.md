# Conversations

## What is the Conversations Report?

The Conversations Report provides detailed analytics about your customer conversations, including response times, resolution times, assignee performance, and conversation volume. Use this report to understand how quickly your team responds to customers and how efficiently conversations are resolved.

## When to use it?

* **Performance Review**: Analyze team response times and identify areas for improvement.
* **Workload Analysis**: See which team members are handling the most conversations.
* **Customer Experience**: Track how long customers wait for responses and resolutions.
* **Trend Analysis**: Monitor conversation volume and response patterns over time.

## How to use it (Step by Step)

{% stepper %}
{% step %}
#### Open Conversations Report

Go to `Reports` > `Conversations` from the left menu.

<figure><img src="../.gitbook/assets/Screenshot 2026-02-13 at 3.52.06 PM.png" alt=""><figcaption></figcaption></figure>

> \[Screenshot: Conversations report page with date range selector at the top]
{% endstep %}

{% step %}
#### Select Date Range

Choose a date range using the preset options (Last 7 days, Last 30 days, This month, This year) or click the date picker to select a custom range.

<figure><img src="../.gitbook/assets/Screenshot 2026-02-13 at 3.52.06 PM (1).png" alt=""><figcaption></figcaption></figure>

> \[Screenshot: Date range selector with preset options and custom date picker]
{% endstep %}

{% step %}
#### Review Overview Charts

At the top of the page, you'll see three key charts:

* Opened vs Closed Conversations: Shows the volume of conversations opened and closed over the selected period.
* Response Time: Displays average response times, with options to compare specific team members.
* Resolution Time: Shows how long it takes to resolve conversations, with a note that conversations must be manually closed to be tracked.

<div><figure><img src="../.gitbook/assets/Screenshot 2026-02-13 at 3.52.40 PM.png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/Screenshot 2026-02-13 at 3.52.45 PM.png" alt=""><figcaption></figcaption></figure></div>

> \[Screenshot: Three charts showing opened vs closed, response time, and resolution time]
{% endstep %}

{% step %}
#### Compare Team Members (Optional)

To compare specific team members' performance:

1. Scroll to the Response Time or Resolution Time chart.
2. Click "Select an assignee to compare" below the chart.
3. Select one or two team members from the dropdown.
4. The chart will update to show their individual performance lines.

<figure><img src="../.gitbook/assets/Screenshot 2026-02-13 at 3.53.03 PM.png" alt=""><figcaption></figcaption></figure>

> \[Screenshot: Assignee selector dropdown and updated chart with multiple lines for comparison]
{% endstep %}

{% step %}
#### View Conversation List

Scroll down to the "Conversation List" table, which shows detailed information for each conversation. Use the tabs at the top to filter by:

* Overall Response Time: Conversations with first responses in the selected period.
* \[Team Member]'s Response Time: Conversations where a specific team member responded.
* Overall Resolution Time: Conversations closed in the selected period.
* \[Team Member]'s Resolution Time: Conversations closed by a specific team member.

<figure><img src="../.gitbook/assets/Screenshot 2026-02-13 at 3.56.18 PM.png" alt=""><figcaption></figcaption></figure>

> \[Screenshot: Conversation List table with tabs for different views]
{% endstep %}

{% step %}
#### Review Conversation Details

Each row in the table shows:

* Contact: Customer name (clickable link to their contact profile).
* Conversation Time Window: When the conversation was opened and closed, and by whom.
* First Response Time: How long it took to send the first response, and who sent it.
* First Assignee: The first team member assigned, their response time, and resolution time.
{% endstep %}

{% step %}
#### Export Data (Optional)

Click the Export button at the top right of the Conversation List table to download an Excel file with all conversation data for the selected date range and tab.
{% endstep %}
{% endstepper %}

## Export and Filter Options

Each row in the table shows:

* Contact: Customer name (clickable link to their contact profile).
* Conversation Time Window: When the conversation was opened and closed, and by whom.
* First Response Time: How long it took to send the first response, and who sent it.
* First Assignee: The first team member assigned, their response time, and resolution time.
* Last Assignee: The last team member assigned, their response time, and resolution time.
* **Total Resolution Time**: Overall duration and assignee-involved duration.
* **Last Assigned List**: The inbox tab where the conversation was last assigned.
* **Tagging Activity**: Tags added or removed during the conversation (hover to see timeline).
* **Custom Attributes**: Any custom attribute values associated with the contact.

## What happens after you use it?

* **Data Displayed**: The report shows all conversations matching your selected filters and date range.
* **Charts Updated**: Overview charts reflect the selected period and any team member comparisons.
* **Export Generated**: If you clicked Export, an Excel file downloads with detailed conversation data.

## Understanding Conversation Metrics

### Conversation Lifecycle Events

Every conversation goes through key lifecycle events that are tracked in the report:

* **Conversation Opened**:
  * **When**: The time of the first incoming message from either the customer or your team that starts a new conversation.
  * **Who**: The person or system that sent the first message.
  * **Note**: A new conversation is only opened when there is no ongoing conversation. If a customer sends a message and there's already an active conversation, it continues that conversation instead of opening a new one.
* **Conversation Closed**:
  * **When**: The time when someone manually closes the conversation using the "Close Conversation" button.
  * **Who**: The team member who closed the conversation.
  * **Note**: Conversations must be manually closed to be tracked. Open conversations are not included in resolution time calculations.
* **First Response**:
  * **When**: The time when the first message is sent from your side (team member, automation, or system) after the customer's first message.
  * **Who**: The person or system that sent the first response (could be a team member, automation, workflow, or other system entity).
  * **Note**: This is the first reply from your side, regardless of whether it's from a human or automated system.
* **First Assignee**:
  * **When**: The time when the first human team member is assigned to the conversation, and when they first responded after being assigned.
  * **Who**: The first human team member assigned to handle the conversation.
  * **Note**: Only human team members count as assignees. Automated systems (automations, workflows) do not count as assignees.
* **Last Assignee**:
  * **When**: The time when the most recent human team member is assigned (if the conversation was handed off), and when they first responded after being assigned.
  * **Who**: The most recent human team member assigned to the conversation.
  * **Note**: If a conversation is reassigned multiple times, this shows only the most recent assignee, not all previous assignees.

### Time Calculations

The report calculates two types of time durations:

**Standard Time (24-hour calculation)**:

* **First Response Time**: Time from when conversation opened to when first response was sent.
* **Process Time**: Total time from when conversation opened to when it was closed.
* **Human Process Time**: Time from when first assignee was assigned to when conversation was closed.
* **Assignment Response Time**: Time from when first assignee was assigned to when they first responded.
* **Last Assignment Response Time**: Time from when last assignee was assigned to when they first responded.

**Working Hours Time (SLA calculation)**:

* Calculated based on working hours profiles when available.
* **For Team Members**: Uses the assignee's personal working hours profile, or team working hours if no personal profile is set.
* **For Automated Systems**: Always calculated using 24-hour time (no working hours applied).
* **Which Profile is Used**: Depends on who performed the action. For example:
  * If Assignee A sent the first response, Assignee A's working hours profile is used.
  * If Assignee B closed the conversation, Assignee B's working hours profile is used for closing time calculations.

**Note**: Working hours time is preferred when available because it gives a more accurate picture of actual response performance during business hours.

### Who Can Respond to Conversations?

The report tracks different types of responders:

* **User**: The customer or contact who is messaging you.
* **WA Owner**: Any activity from WhatsApp mobile app or linked devices that's not going through Luluchat (e.g., someone using the WhatsApp mobile app directly on the phone number).
* **Team User Name**: Your human team members who are assigned to conversations.
* **Automation**: Messages sent automatically by Message Flows.
* **Workflow**: Messages sent automatically by Workflows.
* **Webhook**: Messages sent via webhook API calls triggered by your business systems.
* **Broadcast**: Messages sent via the Broadcast feature.

**Important**: Only human team members (Team User Name) count as assignees for assignee-related metrics. Automated systems (Automation, Workflow, Webhook, Broadcast) can send responses but don't count as assignees.

### Conversation Timeline Example

Here's how a typical conversation timeline works:

1. **Customer sends first message** → Conversation is **Opened** (opened time recorded).
2. **Your team or automation responds** → **First Response** time is calculated (time from opened to first response).
3. **Team member A is assigned** → **First Assignee** is recorded (Assignee A, assignment time recorded).
4. **Assignee A responds** → **First Assignee Response Time** is calculated (time from assignment to response).
5. **Conversation is reassigned to Team member B** → **Last Assignee** is updated (Assignee B, new assignment time recorded).
6. **Assignee B responds** → **Last Assignee Response Time** is calculated (time from B's assignment to B's response).
7. **Assignee B closes conversation** → Conversation is **Closed** (closed time recorded, resolution time calculated).

**Note**: If a conversation is reassigned, the "Last Assignee Response Time" resets and starts counting from the new assignment time, not from the original assignment.

## Important behavior to know

* **Working Hours vs Total Time**: Response and resolution times can show "working hours" (excluding non-working hours) or "total time" (including all hours). Working hours are preferred when available.
* **Manual Close Required**: Resolution time only tracks conversations that were manually closed using the "Close Conversation" button in the Inbox. Conversations that remain open are not included in resolution time metrics.
* **First vs Last Assignee**: If a conversation was reassigned, you'll see both the first and last assignee with their respective response and resolution times.
* **Assignee Reset**: When a conversation is reassigned, the "Last Assignee Response Time" resets and starts counting from the new assignment, not from the original assignment.
* **Automated Responses**: Automated systems (Message Flows, Workflows, etc.) can send the first response, but only human team members count as assignees.
* **New Conversation Rule**: A new conversation is only opened when there's no ongoing conversation. If a customer sends a message while a conversation is still open, it continues the existing conversation.
* **Tag Timeline**: Hover over the tagging activity column to see a timeline of when tags were added or removed.
* **Sortable Columns**: Many columns can be sorted by clicking the column header.
* **Tab-Specific Filters**: The conversation list filters change based on which tab you select (Response Time vs Resolution Time).

## Common issues & solutions

* **No data showing**:
  * Check that your date range includes periods when conversations occurred.
  * Ensure you've selected the correct tab (Response Time vs Resolution Time).
  * Verify that conversations were actually opened/closed in the selected period.
* **Resolution time not tracking**:
  * Resolution time only tracks conversations that were manually closed. Make sure team members are using the "Close Conversation" button in the Inbox.
* **Can't compare team members**:
  * You need to select at least one assignee using the dropdown below the Response Time or Resolution Time chart.
  * The comparison only works if those team members have activity in the selected date range.
* **Export file is empty**:
  * Check that you've selected a date range with actual conversation data.
  * Verify you're on the correct tab (the export matches the active tab's filter).

## Best practice 💡

* **Regular Reviews**: Check this report weekly or monthly to identify trends and performance issues.
* **Team Comparisons**: Use the assignee comparison feature to identify top performers and team members who may need additional support.
* **Close Conversations**: Train your team to manually close conversations to ensure accurate resolution time tracking.
* **Export for Analysis**: Export data regularly for deeper analysis in Excel or other tools.
* **Date Range Selection**: Use appropriate date ranges—shorter ranges (7-30 days) for recent performance, longer ranges (year) for trend analysis.

## Related Documentation

* [Close Conversation](../inbox/close-conversation.md) - Learn how to properly close conversations for accurate tracking
* [Team Users Report](team-users.md) - View individual team member performance summaries
