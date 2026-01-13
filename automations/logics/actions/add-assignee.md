# Add Assignee

## What is Add Assignee?
Assigns the conversation to selected team members when this Action runs in a Message Flow.

## When does it trigger?
- When the flow reaches this `Add Assignee` action while the flow is active and the channel is connected.

## How to set it up (Step by Step)

### Step 1: Open the flow and edit the Action node
In `Automations` > `Message Flows`, open a flow, select the `Action` step, and choose `Add Assignee`.

📸 Screenshot placeholder:
> [Screenshot: Action step showing the Add Assignee option]

### Step 2: Select assignees and save
Pick one or more team members to assign the conversation to, then save the Action block.

📸 Screenshot placeholder:
> [Screenshot: Add Assignee action form with user selector]

## What happens after it triggers?
The conversation is assigned to the chosen users; routing follows your inbox rules and the flow continues.

## Important behavior to know
- Only available users can be assigned; permissions may hide some members.
- If multiple assignees are added, all appear on the conversation.

## Common issues & solutions
- No assignment: ensure the action is on a published path and the channel is connected.
- User not listed: check that the teammate has access to the workspace/channel.

## Best practice 💡
- Assign to a role-based user group or round-robin before adding specific assignees when possible.
- Keep assignments close to where the conversation context is clear.
