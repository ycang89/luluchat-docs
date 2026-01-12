# Opt Out

## What is Opt Out?
Marks the contact as opted out of messaging when this Action runs.

## When does it trigger?
- When the flow reaches this `Opt Out` action while the flow is active and the channel is connected.

## How to set it up (Step by Step)

### Step 1: Open the flow and edit the Action node
In `Automations` > `Message Flows`, open a flow, select the `Action` step, and choose `Opt Out`.

📸 Screenshot placeholder:
> [Screenshot: Action step showing the Opt Out option]

### Step 2: Place it on unsubscribe paths
Add this action where users request to stop messages (e.g., after an “opt-out” keyword), then save and publish.

📸 Screenshot placeholder:
> [Screenshot: Flow path showing Opt Out action on an unsubscribe branch]

## What happens after it triggers?
The contact’s opt-out status is set, preventing further messaging until they opt in again; the flow continues along the path you set.

## Important behavior to know
- Opt-out status overrides other messaging actions for the contact.
- Use alongside a confirmation message so users know they’ve been unsubscribed.

## Common issues & solutions
- Contact still receives messages: confirm downstream flows respect opt-out and that opt-out runs on the published path.

## Best practice 💡
- Provide a clear confirmation and a way to re-opt in if appropriate.
- Keep opt-out paths simple to avoid accidental sends afterward.
