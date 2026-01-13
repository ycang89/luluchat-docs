# Remove Tag

## What is Remove Tag?
Removes selected tags from the contact when this Action runs in a Message Flow.

## When does it trigger?
- When the flow reaches this `Remove Tag` action while the flow is active and the channel is connected.

## How to set it up (Step by Step)

### Step 1: Open the flow and edit the Action node
In `Automations` > `Message Flows`, open a flow, select the `Action` step, and choose `Remove Tag`.

📸 Screenshot placeholder:
> [Screenshot: Action step showing the Remove Tag option]

### Step 2: Choose tags to remove
Select the tags to remove from the contact, then save the Action block.

📸 Screenshot placeholder:
> [Screenshot: Remove Tag action form with tag selector]

## What happens after it triggers?
The chosen tags are removed from the contact record; the flow continues to the next step.

## Important behavior to know
- Only the selected tags are removed; other tags stay unchanged.
- Requires an active channel and a published flow path to execute.

## Common issues & solutions
- Tag still present: confirm the contact had the tag and the action sits on the published path.
- Cannot find a tag: verify the tag exists and you have access to it.

## Best practice 💡
- Remove tags you no longer want to drive routing or reporting.
- Pair with `Add Tag` in the same flow to keep states tidy.
