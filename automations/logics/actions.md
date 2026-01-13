# Logic: Actions

## What is the Actions Node?
The Actions node is a background step that performs specific tasks without sending a message to the customer. It is used to organize your workspace, update contact data, and trigger external events.

## When to use it?
- To categorize contacts by adding or removing **Tags**.
- To assign a conversation to a specific **Assignee** or add **Collaborators**.
- To update **Custom Attributes** based on the customer's journey.
- To trigger external systems via a **Webhook**.
- To manage opt-in/opt-out status.

## How to set it up (Step by Step)
1. In the Message Flow Editor, click **Add Node (+) > Logics > Actions**.
2. Click on the node to open the configuration drawer.
3. Click **Add Action** to select from the library of available actions.
4. Configure the details for each action (e.g., select the tag name or assignee).
5. You can add multiple actions within a single node; they will be executed in order.

📸 Screenshot placeholder:
> [Screenshot: Actions node configuration drawer showing multiple actions added]

## Actions Library
For detailed information on each specific action, please refer to the [Actions Library](./actions/index.md).

## What happens after it triggers?
All actions within the node are executed immediately and in order (from top to bottom). The contact's profile, tags, and assignments are updated instantly, and the flow continues to the next step.

## Important behavior to know
- **Execution Order**: Actions are performed in the exact order they appear in the list, from top to bottom.
- **Instant Updates**: Changes to tags, assignments, or custom attributes take effect immediately and are visible to all team members.
- **Webhook Timing**: External webhooks are sent asynchronously; the flow continues even if your server takes time to respond.

## Common issues & solutions
- **Multiple actions not working**: Ensure all actions are properly configured. You can add as many actions as needed in a single node (e.g., "Add Tag: New Lead", "Assign: Sales Team", and "Update Attribute: Source=WhatsApp").
- **Assignment not visible**: Assignments happen immediately. If a teammate doesn't see the conversation, check that the action was saved and the flow was published.
- **Webhook not received**: Luluchat will attempt to send the webhook to your URL. If your server returns an error, the flow continues to the next step. Check your server logs to see if the request was received.

## Best practice 💡
- **Silent Tagging**: Use actions to tag customers based on the paths they choose in a flow. This helps you build detailed audience segments without interrupting the conversation.
- **Auto-Assignment**: Combine actions with "Start Flow" to automatically route high-priority leads to the right team members.
