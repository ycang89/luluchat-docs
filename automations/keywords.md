# Keywords

## What is the Keywords Page?
The Keywords page is a management dashboard that shows you all keyword triggers configured across all your Message Flows. It provides a centralized view to see which keywords trigger which flows, making it easy to review, search, and manage your keyword automation setup.

## When to use it?
- **Review All Keywords**: See all keyword triggers across your entire account in one place.
- **Find Conflicts**: Quickly identify if multiple flows are using the same or overlapping keywords.
- **Edit Keywords**: Click "Edit" on any keyword to jump directly to its Message Flow's Starting Step.
- **Export Your List**: Download a spreadsheet of all keywords for backup or analysis.

## How to use it (Step by Step)

### Step 1: Open Keywords Page
Go to `Automations` > `Keywords` from the left menu.

📸 Screenshot placeholder:
> [Screenshot: Keywords page showing a list of keyword entries with their match conditions and linked flows]

### Step 2: Review Your Keywords
Each row in the list shows:
- **Match Condition**: How the keyword is matched (is, contain, contain all, begin with, end with).
- **Keywords**: The actual words or phrases (displayed as tags).
- **Linked Flow**: Which Message Flow will start when this keyword is triggered.
- **Edit Button**: Click to open the flow's Starting Step and modify the keyword trigger.

📸 Screenshot placeholder:
> [Screenshot: A keyword list item showing "Message contain [sales, discount] tags" and the linked flow name]

### Step 3: Search for Keywords
Use the search box at the top right to find specific keywords across all flows.

📸 Screenshot placeholder:
> [Screenshot: Search box in the Keywords page header]

### Step 4: Export Your List (Optional)
Click the **Export** button to download an Excel file containing all your keywords and their linked flows.

📸 Screenshot placeholder:
> [Screenshot: Export button in the Keywords page header]

## What happens after you use it?
- **Viewing**: You can see all your keyword configurations at a glance.
- **Editing**: Clicking "Edit" takes you directly to the Message Flow editor where you can modify the keyword trigger in the Starting Step.
- **Exporting**: You receive an Excel file with all keyword data for offline review or backup.

## Important behavior to know
- **Read-Only View**: This page shows keywords but doesn't allow direct editing. To change a keyword, click "Edit" to open the flow's Starting Step.
- **All Flows**: The list includes keywords from all Message Flows in your account, not just active ones.
- **Search Functionality**: The search box filters keywords by the actual keyword text, not by flow name.

## Common issues & solutions
- **Can't find a keyword**: Use the search box to filter the list. Remember that keywords are case-insensitive, so search for any variation.
- **Want to add a new keyword**: Keywords are added in the Message Flow's Starting Step, not on this page. Go to `Automations` > `Message Flows` and edit the flow you want.
- **See duplicate keywords**: If multiple flows have the same keyword, they will all appear in the list. The first matching flow will trigger when a customer sends that message.

## Best practice 💡
- **Regular Reviews**: Check this page monthly to identify and remove unused keywords or resolve conflicts.
- **Export Before Changes**: Export your keyword list before making major changes as a backup.
- **Use Search**: When managing many keywords, use the search function to quickly find specific entries.

## Related Documentation
To learn how to configure keyword triggers, see [Trigger (Starting Step)](./steps/trigger.md#1-keyword-trigger).
