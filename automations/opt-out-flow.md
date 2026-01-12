# Opt-Out Flow

## What is Opt-Out Flow?
Handles unsubscribe requests, marks the contact as opted out, and confirms they will no longer receive messages unless they re-opt in.

## When does it trigger?
- When the flow is invoked on an opt-out path (e.g., via keyword/trigger/manual run) to process an unsubscribe request.

## How to set it up (Step by Step)

### Step 1: Open Message Flows
Go to `Automations` → `Message Flows` and create/select the Opt-Out Flow.

📸 Screenshot placeholder:
> [Screenshot: Message Flows list showing Opt-Out Flow]

### Step 2: Confirm unsubscribe
Include a clear confirmation message (“You’ve been unsubscribed”). Save/publish.

📸 Screenshot placeholder:
> [Screenshot: Opt-Out Flow builder with unsubscribe confirmation]

### Step 3: Update status
Ensure the flow includes the opt-out action/update so the contact is marked as opted out.

📸 Screenshot placeholder:
> [Screenshot: Action step marking opt-out]

## What happens after it triggers?
The contact is marked opted out; further messaging should stop until they opt in again.

## Important behavior to know
- Opt-out overrides other messaging; respect it across automations.
- Provide a path to re-opt in if appropriate (per policy).

## Common issues & solutions
- Messages still sending: verify opt-out status is applied and automations respect it.
- Trigger not firing: ensure the opt-out keyword/path is set and the flow is published.

## Best practice 💡
- Keep the confirmation concise; avoid additional marketing content.
- Log or tag the source of opt-out for compliance.
