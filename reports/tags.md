# Reports: Tags

## What is the Tags Report?
The Tags Report tracks tag growth and usage over time, showing how many contacts have been tagged or untagged during a selected period. Use this report to understand tag adoption, identify popular tags, and see which contacts are associated with specific tags.

## When to use it?
- **Tag Strategy**: Monitor which tags are being used most frequently.
- **Contact Segmentation**: See how your contact segmentation (via tags) is evolving.
- **Campaign Analysis**: Track tag changes related to specific campaigns or initiatives.
- **Growth Tracking**: Monitor tag adoption trends over time.

## How to use it (Step by Step)

### Step 1: Open Tags Report
Go to `Reports` > `Tags` from the left menu.

📸 Screenshot placeholder:
> [Screenshot: Tags report page with date range selector]

### Step 2: Select Date Range
Choose a date range using the preset options (Last 7 days, Last 30 days, This month, This year) or select a custom range using the date picker.

📸 Screenshot placeholder:
> [Screenshot: Date range selector with options]

### Step 3: Select Tags to Analyze
In the "Select Tags" section, choose one or more tags from the dropdown. You can select multiple tags to compare their growth patterns. The report will show data only for the selected tags.

📸 Screenshot placeholder:
> [Screenshot: Tag selector dropdown with multiple tags selected]

**Note**: If no tags are selected, the charts and tables will be empty. At least one tag must be selected to view data.

### Step 4: Review Tag Growth Chart
The "All-Time Cumulative Tags" chart shows the cumulative growth of selected tags over time. Each tag appears as a separate line, making it easy to compare growth rates.

📸 Screenshot placeholder:
> [Screenshot: Line chart showing cumulative tag growth with multiple tag lines]

### Step 5: View Tag Changes Table
Below the chart, the "Tag Changes" table shows:
- **Name**: The tag name.
- **Added this period**: Number of contacts that received this tag during the selected period.
- **Removed this period**: Number of contacts that had this tag removed during the selected period.

📸 Screenshot placeholder:
> [Screenshot: Tag Changes table with columns for name, added, and removed counts]

### Step 6: View Contact Lists (Optional)
Click the "More" button on any tag row to expand and see detailed contact lists:
- **Added Contact List**: Shows all contacts that received this tag during the selected period.
- **Removed Contact List**: Shows all contacts that had this tag removed during the selected period.

Each contact list shows:
- Contact name (clickable to view profile)
- Contact number
- Link to open the conversation in Inbox

📸 Screenshot placeholder:
> [Screenshot: Expanded tag row showing tabs for Added and Removed contact lists]

### Step 7: Export Data (Optional)
Click the **Export** button in the Tag Changes table toolbar to download an Excel file with tag change data.

📸 Screenshot placeholder:
> [Screenshot: Export button in the table toolbar]

## What happens after you use it?
- **Charts Displayed**: The cumulative growth chart updates to show selected tags.
- **Table Populated**: The Tag Changes table shows added/removed counts for selected tags.
- **Contact Lists Available**: Expanded rows show detailed contact information for tag changes.

## Important behavior to know
- **Tag Selection Required**: You must select at least one tag to see any data. The report doesn't show all tags by default.
- **Cumulative Growth**: The chart shows cumulative totals (all-time), not just the selected period. This means the line always trends upward or stays flat—it never decreases.
- **Period-Specific Changes**: The "Added this period" and "Removed this period" columns only count changes that occurred within your selected date range.
- **Contact Lists**: The expanded contact lists are paginated, so you can browse through all contacts that had tag changes.

## Common issues & solutions
- **No data showing**:
  - Make sure you've selected at least one tag from the dropdown.
  - Check that your date range includes periods when tag changes occurred.
  - Verify that the selected tags actually exist and have been used.

- **Chart shows no lines**:
  - Ensure tags are selected and that those tags have activity in the selected date range.
  - Try expanding your date range to include more historical data.

- **Can't find a specific tag**:
  - All available tags appear in the dropdown. If a tag doesn't appear, it may not exist yet—create it in Settings > Tags first.

- **Contact lists are empty**:
  - This means no contacts had the selected tag added or removed during the selected period.
  - Try expanding your date range or selecting different tags.

## Best practice 💡
- **Regular Monitoring**: Check tag growth weekly to understand how your contact segmentation is evolving.
- **Compare Tags**: Select multiple tags to compare their adoption rates and identify which tags are most effective.
- **Review Contact Lists**: Use the expanded contact lists to verify that tags are being applied correctly.
- **Export for Analysis**: Export tag change data to analyze trends in Excel or other tools.
- **Tag Naming**: Use consistent tag naming conventions to make reports easier to interpret.

## Related Documentation
- [Tags Settings](./../settings/data/tags.md) - Learn how to create and manage tags
- [Add Tags in Inbox](./../inbox/contact-info/profile.md) - See how to tag contacts during conversations
