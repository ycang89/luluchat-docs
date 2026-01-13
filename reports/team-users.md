# Team Users

## What is the Team Users Report?

The Team Users Report provides performance metrics for each team member, including conversation assignments, resolutions, response times, and workload distribution. Use this report to evaluate individual team member performance, identify training needs, and balance workloads.

## When to use it?

* **Performance Reviews**: Assess individual team member productivity and response times.
* **Workload Balancing**: Identify team members who are overloaded or underutilized.
* **Training Needs**: Spot team members who may need additional support or training.
* **Team Planning**: Make data-driven decisions about team size and resource allocation.

## How to use it (Step by Step)

{% stepper %}
{% step %}
#### Open Team Users Report

Go to `Reports` > `Team Users` from the left menu.

📸 Screenshot placeholder:

> \[Screenshot: Team Users report page with date range selector]
{% endstep %}

{% step %}
#### Select Date Range

Choose a date range using the preset options (Last 7 days, Last 30 days, This month, This year) or select a custom range using the date picker.

📸 Screenshot placeholder:

> \[Screenshot: Date range selector with preset and custom options]
{% endstep %}

{% step %}
#### Review Performance Table

The main table shows performance metrics for each team member and system entities. Each row displays:

* Name: Team member name or system entity (AI Agent, Broadcast, Automation, Workflow, Webhook, WA Owner). Some names have tooltips explaining what they represent.
* Conversation Assigned: Total number of conversations assigned to this person/entity.
* Conversation Resolved: Total number of conversations closed/resolved.
* Contact Assigned: Number of unique contacts assigned.
* Contact Resolved: Number of unique contacts whose conversations were resolved.
* Average First Response Time: Average time to send the first response after assignment.
* Average Resolution Time: Average time to resolve (close) conversations.
* Max Response Time: Longest time taken to send a first response.
* Max Resolution Time: Longest time taken to resolve a conversation.

📸 Screenshot placeholder:

> \[Screenshot: Team Users performance table with all columns visible]
{% endstep %}

{% step %}
#### Understand System Entities

Some rows represent system entities rather than human team members:

* AI Agent: Messages sent by the AI Agent feature.
* Broadcast: Messages sent via broadcasts.
* Automation: Messages sent by Message Flows.
* Workflow: Messages sent by Workflows.
* Webhook: Messages sent via webhook API calls.
* WA Owner: Activity from WhatsApp mobile app or linked devices (not through Luluchat).

Hover over the name to see a tooltip explaining what each entity represents.

📸 Screenshot placeholder:

> \[Screenshot: Tooltip showing explanation for "AI Agent" entity]
{% endstep %}

{% step %}
#### Export Data (Optional)

Click the Export button at the top right of the table to download an Excel file with all team user performance data for the selected date range.

📸 Screenshot placeholder:

> \[Screenshot: Export button in the table toolbar]
{% endstep %}
{% endstepper %}

## What happens after you use it?

* **Table Populated**: The performance table displays all team members and system entities with their metrics.
* **Data Filtered**: All metrics reflect only activity within the selected date range.
* **Export Generated**: If you clicked Export, an Excel file downloads with detailed performance data.

## Important behavior to know

* **Working Hours vs Total Time**: Response and resolution times prioritize "working hours" (excluding non-working hours) when available, falling back to "total time" if working hours aren't configured.
* **System Entities Included**: The report includes automated systems (AI Agent, Broadcasts, etc.) alongside human team members, giving you a complete picture of message sources.
* **Unique Contacts**: "Contact Assigned" and "Contact Resolved" count unique contacts, not total conversations. One contact can have multiple conversations.
* **Date Range Impact**: All metrics are calculated based on activity within your selected date range. Changing the range will update all numbers.
* **Max Times**: The "Max Response Time" and "Max Resolution Time" show the longest individual instance, which may be an outlier.

## Common issues & solutions

* **Team member not appearing**:
  * Check that the team member had activity (assignments or resolutions) during the selected date range.
  * Verify the team member exists in Settings > Users.
* **All metrics show "-"**:
  * This means the person/entity had no activity in the selected date range.
  * Try expanding your date range to include more historical data.
* **Response times seem incorrect**:
  * Response times are calculated from when a conversation is assigned to when the first message is sent.
  * Working hours are used when available, which may make times appear shorter than expected.
* **System entities showing high numbers**:
  * This is normal—automated systems (Broadcasts, Automations) can handle many conversations.
  * Use this data to understand the balance between automated and human responses.

## Best practice 💡

* **Regular Reviews**: Check this report weekly or monthly to track team performance trends.
* **Compare Metrics**: Look at both average and max times to identify outliers and training opportunities.
* **Balance Workloads**: Use "Conversation Assigned" to ensure work is distributed evenly across team members.
* **Set Goals**: Use average response and resolution times to set team performance goals.
* **Export for Analysis**: Export data regularly to track performance trends over time in Excel.
* **Consider System Entities**: Remember that automated systems handle many conversations—this is expected and helps scale your support.

## Related Documentation

* [Users Settings](../settings/account/users.md) - Learn how to manage team members
* [Conversations Report](conversations.md) - View detailed conversation-level analytics
* [Close Conversation](../inbox/close-conversation.md) - Ensure conversations are properly closed for accurate tracking
