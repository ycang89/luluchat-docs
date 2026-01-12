# Add Tag

## What is Add Tag?
Adds one or more tags to the contact when this Action runs in a Message Flow.

## When does it trigger?
- When the flow reaches this Action node while the flow is active and the channel is connected.

## How to set it up (Step by Step)

### Step 1: Open the flow and edit the Action node
In `Automations` > `Message Flows`, open a flow and select the `Action` step. Click `Add Tag`.

📸 Screenshot placeholder:
> [Screenshot: Action step showing the Add Tag option]

### Step 2: Choose tags
Pick one or more tags to apply to the contact, then save the Action block.

📸 Screenshot placeholder:
> [Screenshot: Add Tag action form with tag selector]

## What happens after it triggers?
The selected tags are added to the contact immediately; the flow continues to the next step.

## Important behavior to know
- Tags apply to the contact record for the current channel/team.
- Duplicate tags are ignored if already present.

## Common issues & solutions
- Tag not applied: confirm the action is in the published flow path and the channel is connected.
- Cannot find a tag: create the tag first or check access to tags.

## Best practice 💡
- Use consistent tag naming for reporting and filters.
- Apply only the tags needed for routing or segmentation.
