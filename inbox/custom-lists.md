# Custom Lists

## What is Custom Lists?
Custom Lists allow you to organize conversations into custom categories that you create. Unlike the default inbox lists (All, Awaiting Reply, Unread, etc.), custom lists let you create your own groupings, such as "VIP Customers", "Pending Orders", or "Follow-up Needed". You can add or remove conversations from these lists to keep your inbox organized and easily find specific conversations.

## Default System Lists

Luluchat provides several default system lists that automatically organize your conversations based on their status and type. These lists cannot be edited, deleted, or hidden, but they help you quickly find conversations that need attention.

{% tabs %}
{% tab title="Active Conversations" %}
| List Name | Description | When to Use |
|-----------|-------------|-------------|
| **All** | All chats that are not Closed or Archived | Use this list to focus on the most important chats. This is your main working view, showing all active conversations that require attention. |
| **Needs Reply** | Chats you have yet to respond to | Find conversations where the customer has sent a message but you haven't replied yet. Use this to ensure you don't miss any customer inquiries. |
| **Unread** | Chats that have unread messages | Quickly identify conversations with messages you haven't read yet. Helps you prioritize conversations that need your immediate attention. |
{% endtab %}

{% tab title="Status-Based" %}
| List Name | Description | When to Use |
|-----------|-------------|-------------|
| **Awaiting Reply** | Chats that you have not received a response to | Track conversations where you've sent a message but haven't received a reply yet. Use this to monitor conversations waiting for customer responses. |
| **Closed** | Chats that have been marked Closed | View conversations you've closed. Closed conversations are removed from your main "All" list to keep your active inbox clean. **Important**: When you receive a new message from a closed chat, it will be automatically reopened and moved back to your active lists. |
| **Archived** | Chats that have been archived | Access conversations you've manually archived. Archived conversations are hidden from your main inbox view but can be accessed from this list when needed. |
{% endtab %}

{% tab title="Conversation Type" %}
| List Name | Description | When to Use |
|-----------|-------------|-------------|
| **Groups** | Conversations that you have with 3 or more people | Filter to show only group conversations. Makes it easy to manage team chats and group discussions separately from one-on-one conversations. |
| **1:1** | All 1:1 conversations | Focus on individual conversations between you and a single contact. Use this to work on personal customer interactions without group chat distractions. |
{% endtab %}
{% endtabs %}

## When to use it?
- **Organize by Priority**: Create lists for high-priority customers or urgent issues.
- **Project-Based Grouping**: Group conversations related to specific projects or campaigns.
- **Status Tracking**: Create lists for conversations at different stages (e.g., "Awaiting Response", "In Progress").
- **Team Workflows**: Organize conversations by team member responsibilities or departments.
- **Temporary Groupings**: Create lists for time-sensitive campaigns or events.

## How to create a custom list (Step by Step)

{% stepper %}
{% step %}
### Open List Settings
In your Inbox, click the gear icon (⚙️) labeled "List Settings" in the top-right area of the inbox tabs.

📸 Screenshot placeholder:
> [Screenshot: Inbox showing the List Settings gear icon]
{% endstep %}

{% step %}
### Create New List
In the List Settings modal, click the `Add` button to create a new list.

📸 Screenshot placeholder:
> [Screenshot: List Settings modal with Add button]
{% endstep %}

{% step %}
### Enter List Name
In the "New List" modal, enter a name for your custom list (maximum 30 characters). Choose a descriptive name that clearly indicates the purpose of the list.

📸 Screenshot placeholder:
> [Screenshot: New List modal with name input field]
{% endstep %}

{% step %}
### Save the List
Click the submit button to create the list. You'll see a success message confirming the list was created. The new list will appear in your inbox tabs.

📸 Screenshot placeholder:
> [Screenshot: Success message and new list appearing in tabs]
{% endstep %}
{% endstepper %}

## How to manage custom lists (Step by Step)

### Edit a List Name
1. Click the gear icon (⚙️) to open List Settings.
2. Find the list you want to edit in the list.
3. Click the edit icon (✏️) next to the list name.
4. Update the name in the modal and submit.

📸 Screenshot placeholder:
> [Screenshot: List Settings showing edit icon for a list]

### Delete a List
1. Click the gear icon (⚙️) to open List Settings.
2. Find the list you want to delete.
3. Click the delete icon (🗑️) next to the list name.
4. Confirm the deletion in the popup.

**Note**: Deleting a list does not delete the conversations. Conversations will remain in your inbox but will be removed from the deleted list.

📸 Screenshot placeholder:
> [Screenshot: Delete confirmation popup]

### Hide or Show a List
1. Click the gear icon (⚙️) to open List Settings.
2. Find the list you want to hide or show.
3. Click the eye icon (👁️) to hide the list, or the eye-slash icon (👁️‍🗨️) to show it.
4. Hidden lists won't appear in your inbox tabs but can be shown again later.

📸 Screenshot placeholder:
> [Screenshot: List Settings showing hide/show icons]

### Reorder Lists
1. Click the gear icon (⚙️) to open List Settings.
2. Drag and drop lists using the sort handle (⋮⋮) to reorder them.
3. The order you set will be reflected in your inbox tabs.

📸 Screenshot placeholder:
> [Screenshot: Dragging a list to reorder]

## How to add conversations to a list (Step by Step)

### Method 1: From a Conversation

#### Step 1: Open a Conversation
Click on any conversation in your Inbox to open it.

📸 Screenshot placeholder:
> [Screenshot: Conversation opened in Inbox]

{% step %}
### Access List Assignment
Click the three-dot menu (⋮) in the conversation header, then select `List Assignment`.

📸 Screenshot placeholder:
> [Screenshot: Three-dot menu showing "List Assignment" option]
{% endstep %}

{% step %}
### Add to Lists
In the "Add Chat to Lists" modal, you'll see all your custom lists. For each list:
- If the conversation is **not** in the list, click the `Add` button to add it.
- If the conversation is **already** in the list, you'll see a `Remove` button instead.

📸 Screenshot placeholder:
> [Screenshot: Add Chat to Lists modal showing lists with Add/Remove buttons]
{% endstep %}

{% step %}
### Confirm
The conversation is immediately added or removed from the selected list. You'll see a success message confirming the action.
{% endstep %}
{% endstepper %}

### Method 2: Bulk Management from List Settings

{% stepper %}
{% step %}
### Open Manage List
Click the three-dot icon (⋮) on any custom list tab, then select `Manage List`.

📸 Screenshot placeholder:
> [Screenshot: Custom list dropdown showing "Manage List" option]
{% endstep %}

{% step %}
### View Contacts in List
The "Manage List" modal opens, showing all contacts. You can:
- **Search**: Use the search box to find specific contacts.
- **Filter**: Use filters to narrow down contacts by tags, assignee, or other criteria.
- **View Status**: See which contacts are currently in the list (they'll have a "Remove" button) and which are not (they'll have an "Add" button).

📸 Screenshot placeholder:
> [Screenshot: Manage List modal showing contact table with Add/Remove buttons]
{% endstep %}

{% step %}
### Add Contacts Individually
For each contact in the table:
- Click `Add` to add the contact to the list.
- Click `Remove` to remove the contact from the list.
{% endstep %}

{% step %}
### Bulk Add Contacts
1. Select multiple contacts by checking the boxes next to their names.
2. Click the `Bulk Add` button at the bottom of the page.
3. All selected contacts will be added to the list at once.

📸 Screenshot placeholder:
> [Screenshot: Multiple contacts selected with Bulk Add button visible]
{% endstep %}

{% step %}
### Bulk Remove Contacts
1. Select multiple contacts that are already in the list.
2. Click the `Bulk Remove` button at the bottom of the page.
3. All selected contacts will be removed from the list at once.

📸 Screenshot placeholder:
> [Screenshot: Multiple contacts selected with Bulk Remove button visible]
{% endstep %}
{% endstepper %}

## How to remove conversations from a list (Step by Step)

### Method 1: From a Conversation
1. Open the conversation.
2. Click the three-dot menu (⋮) → `List Assignment`.
3. Find the list from which you want to remove the conversation.
4. Click the `Remove` button next to that list.

### Method 2: From List Management
1. Click the three-dot icon (⋮) on the custom list → `Manage List`.
2. Find the contact you want to remove.
3. Click the `Remove` button, or select multiple contacts and click `Bulk Remove`.

## What happens after you add/remove conversations?
- **Immediate Update**: Conversations are immediately added or removed from the list.
- **List View**: When you click on the custom list tab, you'll see only the conversations that are in that list.
- **Search & Filter**: Conversations in custom lists can still be found through search and other filters.
- **No Data Loss**: Removing a conversation from a list does not delete the conversation. It remains in your inbox and other lists where it was added.

{% hint style="info" %}
**Important behavior to know**

- **Custom Lists Only**: You can only add/remove conversations from custom lists you create. Default system lists (All, Awaiting Reply, Unread, Needs Reply, Groups, 1:1, Closed, Archived) are system-managed and automatically update based on conversation status. You cannot manually add or remove conversations from default lists.
- **Multiple Lists**: A conversation can be in multiple custom lists at the same time. Adding it to one list doesn't remove it from others.
- **List Visibility**: Hidden lists don't appear in your inbox tabs but can be managed and shown again from List Settings. Default system lists are always visible and cannot be hidden.
- **List Name Limit**: Custom list names are limited to 30 characters.
- **Bulk Operations**: You can add or remove multiple conversations at once using the bulk actions in the "Manage List" modal.
- **Default Lists**: System default lists (All, Awaiting Reply, Unread, Needs Reply, Groups, 1:1, Closed, Archived) cannot be edited, deleted, or hidden. They automatically update based on conversation properties and status.
- **Automatic Updates**: Default system lists automatically update as conversations change status. For example, when you close a conversation, it automatically appears in "Closed" and disappears from "All". When a closed conversation receives a new message, it automatically reopens and returns to "All".
{% endhint %}

## Common issues & solutions
- **Can't see List Settings button**:
  - Ensure you're in the Inbox module.
  - The List Settings button is the gear icon (⚙️) in the top-right area of the inbox tabs.

- **List not appearing in tabs**:
  - Check if the list is hidden. Go to List Settings and click the eye-slash icon to show it.
  - Refresh the page if the list was just created.

- **Can't add conversation to list**:
  - Ensure you're trying to add to a custom list, not a default system list.
  - Verify the conversation has a contact associated with it (some system messages may not be addable).

- **Bulk Add/Remove not working**:
  - Ensure you've selected at least one contact before clicking the bulk action button.
  - Check that you have the necessary permissions to manage lists.

- **List name too long**:
  - List names are limited to 30 characters. Shorten your list name if you see an error.

- **Can't delete a list**:
  - Only custom lists can be deleted. Default system lists (All, Awaiting Reply, Unread, Needs Reply, Groups, 1:1, Closed, Archived) cannot be deleted.
  - Ensure you're clicking the delete icon on a custom list, not a default one.

- **Conversation not appearing in expected default list**:
  - Default lists automatically filter conversations based on their status. For example, "All" only shows conversations that are not Closed or Archived.
  - Check the conversation's status (closed, archived, read/unread) to understand why it appears or doesn't appear in a specific default list.
  - A conversation can appear in multiple default lists if it matches multiple criteria (e.g., a conversation can be both "Unread" and "Needs Reply").

## Best practice 💡
- **Clear Naming**: Use descriptive names that clearly indicate the list's purpose (e.g., "VIP Customers", "Pending Orders").
- **Regular Cleanup**: Periodically review and remove conversations from lists that are no longer relevant.
- **Use for Organization**: Create lists that align with your workflow and team structure.
- **Limit List Count**: Avoid creating too many lists, as this can make navigation confusing. Focus on the most important groupings.
- **Combine with Tags**: Use custom lists for broad organization and tags for more granular categorization.
- **Team Coordination**: Create lists that help team members quickly find conversations relevant to their work.

## Related Documentation
- [Inbox Overview](./index.md) - Learn about the Inbox module
- [Conversation Controls](./conversation-controls.md) - Learn about other conversation management features
