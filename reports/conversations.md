# Reports: Conversations

## What is the Conversations Report?
The Conversations Report provides detailed analytics about your customer conversations, including response times, resolution times, assignee performance, and conversation volume. Use this report to understand how quickly your team responds to customers and how efficiently conversations are resolved.

## When to use it?
- **Performance Review**: Analyze team response times and identify areas for improvement.
- **Workload Analysis**: See which team members are handling the most conversations.
- **Customer Experience**: Track how long customers wait for responses and resolutions.
- **Trend Analysis**: Monitor conversation volume and response patterns over time.

## How to use it (Step by Step)

### Step 1: Open Conversations Report
Go to `Reports` > `Conversations` from the left menu.

📸 Screenshot placeholder:
> [Screenshot: Conversations report page with date range selector at the top]

### Step 2: Select Date Range
Choose a date range using the preset options (Last 7 days, Last 30 days, This month, This year) or click the date picker to select a custom range.

📸 Screenshot placeholder:
> [Screenshot: Date range selector with preset options and custom date picker]

### Step 3: Review Overview Charts
At the top of the page, you'll see three key charts:
- **Opened vs Closed Conversations**: Shows the volume of conversations opened and closed over the selected period.
- **Response Time**: Displays average response times, with options to compare specific team members.
- **Resolution Time**: Shows how long it takes to resolve conversations, with a note that conversations must be manually closed to be tracked.

📸 Screenshot placeholder:
> [Screenshot: Three charts showing opened vs closed, response time, and resolution time]

### Step 4: Compare Team Members (Optional)
To compare specific team members' performance:
1. Scroll to the Response Time or Resolution Time chart.
2. Click "Select an assignee to compare" below the chart.
3. Select one or two team members from the dropdown.
4. The chart will update to show their individual performance lines.

📸 Screenshot placeholder:
> [Screenshot: Assignee selector dropdown and updated chart with multiple lines for comparison]

### Step 5: View Conversation List
Scroll down to the "Conversation List" table, which shows detailed information for each conversation. Use the tabs at the top to filter by:
- **Overall Response Time**: Conversations with first responses in the selected period.
- **[Team Member]'s Response Time**: Conversations where a specific team member responded.
- **Overall Resolution Time**: Conversations closed in the selected period.
- **[Team Member]'s Resolution Time**: Conversations closed by a specific team member.

📸 Screenshot placeholder:
> [Screenshot: Conversation List table with tabs for different views]

### Step 6: Review Conversation Details
Each row in the table shows:
- **Contact**: Customer name (clickable link to their contact profile).
- **Conversation Time Window**: When the conversation was opened and closed, and by whom.
- **First Response Time**: How long it took to send the first response, and who sent it.
- **First Assignee**: The first team member assigned, their response time, and resolution time.
- **Last Assignee**: The last team member assigned, their response time, and resolution time.
- **Total Resolution Time**: Overall duration and assignee-involved duration.
- **Last Assigned List**: The inbox tab where the conversation was last assigned.
- **Tagging Activity**: Tags added or removed during the conversation (hover to see timeline).
- **Custom Attributes**: Any custom attribute values associated with the contact.

📸 Screenshot placeholder:
> [Screenshot: Expanded conversation row showing all detail columns]

### Step 7: Export Data (Optional)
Click the **Export** button at the top right of the Conversation List table to download an Excel file with all conversation data for the selected date range and tab.

📸 Screenshot placeholder:
> [Screenshot: Export button in the Conversation List toolbar]

## What happens after you use it?
- **Data Displayed**: The report shows all conversations matching your selected filters and date range.
- **Charts Updated**: Overview charts reflect the selected period and any team member comparisons.
- **Export Generated**: If you clicked Export, an Excel file downloads with detailed conversation data.

## Important behavior to know
- **Working Hours vs Total Time**: Response and resolution times can show "working hours" (excluding non-working hours) or "total time" (including all hours). Working hours are preferred when available.
- **Manual Close Required**: Resolution time only tracks conversations that were manually closed using the "Close Conversation" button in the Inbox. Conversations that remain open are not included in resolution time metrics.
- **First vs Last Assignee**: If a conversation was reassigned, you'll see both the first and last assignee with their respective response and resolution times.
- **Tag Timeline**: Hover over the tagging activity column to see a timeline of when tags were added or removed.
- **Sortable Columns**: Many columns can be sorted by clicking the column header.
- **Tab-Specific Filters**: The conversation list filters change based on which tab you select (Response Time vs Resolution Time).

## Common issues & solutions
- **No data showing**:
  - Check that your date range includes periods when conversations occurred.
  - Ensure you've selected the correct tab (Response Time vs Resolution Time).
  - Verify that conversations were actually opened/closed in the selected period.

- **Resolution time not tracking**:
  - Resolution time only tracks conversations that were manually closed. Make sure team members are using the "Close Conversation" button in the Inbox.

- **Can't compare team members**:
  - You need to select at least one assignee using the dropdown below the Response Time or Resolution Time chart.
  - The comparison only works if those team members have activity in the selected date range.

- **Export file is empty**:
  - Check that you've selected a date range with actual conversation data.
  - Verify you're on the correct tab (the export matches the active tab's filter).

## Best practice 💡
- **Regular Reviews**: Check this report weekly or monthly to identify trends and performance issues.
- **Team Comparisons**: Use the assignee comparison feature to identify top performers and team members who may need additional support.
- **Close Conversations**: Train your team to manually close conversations to ensure accurate resolution time tracking.
- **Export for Analysis**: Export data regularly for deeper analysis in Excel or other tools.
- **Date Range Selection**: Use appropriate date ranges—shorter ranges (7-30 days) for recent performance, longer ranges (year) for trend analysis.

## Related Documentation
- [Close Conversation](./../inbox/close-conversation.md) - Learn how to properly close conversations for accurate tracking
- [Team Users Report](./team-users.md) - View individual team member performance summaries
