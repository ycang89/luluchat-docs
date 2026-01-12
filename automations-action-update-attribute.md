# Update Attribute

## What is Update Attribute?
Sets specific attribute values on the contact when this Action runs, letting you override or change stored data.

## When does it trigger?
- When the flow reaches this `Update Attribute` action while the flow is active and the channel is connected.

## How to set it up (Step by Step)

### Step 1: Open the flow and edit the Action node
In `Automations` > `Message Flows`, open a flow, select the `Action` step, and choose `Update Attribute`.

📸 Screenshot placeholder:
> [Screenshot: Action step showing the Update Attribute option]

### Step 2: Pick attributes and set values
Choose the attributes to change and enter the values you want to store, then save the Action block.

📸 Screenshot placeholder:
> [Screenshot: Update Attribute action form with attribute and value fields]

## What happens after it triggers?
The selected attributes on the contact record are updated to the values you set; the flow continues to the next step.

## Important behavior to know
- This overwrites existing values for the chosen attributes.
- Requires the attributes to exist and be accessible to you.

## Common issues & solutions
- Value not updated: ensure the action sits on the published path and the attribute is valid.
- Attribute not available: create it first or check Data Management permissions.

## Best practice 💡
- Use Update Attribute for definitive values (e.g., status, plan) and Save to Attribute for dynamic captured inputs.
- Keep value formats consistent to aid reporting and filters.
