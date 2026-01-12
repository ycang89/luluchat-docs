# Away Flow

## What is Away Flow?
A flow that replies when your channel is set to “away,” telling contacts you’re unavailable and what to do next.

## When does it trigger?
- When the channel is in away mode/status and a contact messages you.
- Only if an Away Flow is configured and the channel is connected.

## How to set it up (Step by Step)

### Step 1: Open Message Flows
Go to `Automations` → `Message Flows` and select/create the Away Flow.

📸 Screenshot placeholder:
> [Screenshot: Message Flows list showing Away Flow option]

### Step 2: Configure away response
Add a short away message and optional options/links (e.g., expected reply time, alternative contact). Save/publish.

📸 Screenshot placeholder:
> [Screenshot: Away Flow builder with away message]

### Step 3: Enable for away mode
Mark this flow as the Away Flow and ensure your channel away status is set when needed.

📸 Screenshot placeholder:
> [Screenshot: Setting indicating Away Flow assignment]

## What happens after it triggers?
Contacts receive the away response and any follow-up steps you add (menu, capture intent, handoff scheduling).

## Important behavior to know
- Runs only when away status is active.
- Other triggers may be bypassed while away flow handles the initial response.

## Common issues & solutions
- Not firing: confirm away status is on and the flow is assigned as Away.
- Conflicts: check other automations that may still reply; adjust precedence.

## Best practice 💡
- Set clear expectations (when you’ll respond, alternative channels).
- Keep it brief and offer one clear next step (leave info, schedule, or FAQ link).
