# Close Inbox Conversation

## What is Close Inbox Conversation?
Closes the current conversation in the inbox when this Action runs.

## When does it trigger?
- When the flow reaches this `Close Inbox Conversation` action while the flow is active and the channel is connected.

## How to set it up (Step by Step)

### Step 1: Open the flow and edit the Action node
In `Automations` > `Message Flows`, open a flow, select the `Action` step, and choose `Close Inbox Conversation`.

📸 Screenshot placeholder:
> [Screenshot: Action step showing the Close Inbox Conversation option]

### Step 2: Save and publish
Add the action where the conversation should end, then save and publish the flow.

📸 Screenshot placeholder:
> [Screenshot: Flow path showing the Close Inbox Conversation action in the sequence]

## What happens after it triggers?
The conversation is marked closed in the inbox; downstream steps still run if connected after this action.

> [!NOTE]
> **Important behavior to know**
>
> - **Automatic Removal**: Closed conversations are automatically removed from the "All" list and moved to the "Closed" list in your Inbox.
> - **Reopening**: If a closed conversation receives a new message, it will automatically reopen and return to the "All" list.
> - **History Preserved**: Closing does not delete history; it only marks the thread as closed.
> - **Downstream Actions**: If you add steps after this action, they will still execute; place it at the end of the path you want closed.
> - **Assignee Retention**: Depending on your Inbox settings, the assignee may or may not be retained when a conversation is closed.

## Common issues & solutions
- Conversation stayed open: confirm the action is on the published path and the channel is connected.
- Accidentally closed: reopen in the inbox or remove the action in the flow.

## Best practice 💡
- Use close actions at the end of resolutions or opt-out paths.
- Pair with a final confirmation message before closing.
