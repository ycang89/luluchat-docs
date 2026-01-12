# Absent Flow

## What is Absent Flow?
An overflow/queue flow used when your inbox is too busy or agents are unavailable, guiding contacts while they wait.

## When does it trigger?
- When the channel hits an absent/overflow condition (e.g., queue full, offline window) and an Absent Flow is configured.

## How to set it up (Step by Step)

### Step 1: Open Message Flows
Go to `Automations` → `Message Flows` and select/create the Absent Flow.

📸 Screenshot placeholder:
> [Screenshot: Message Flows list showing Absent Flow option]

### Step 2: Configure options
Provide an absent message and optional menu of flows/actions (e.g., “1. Sales flow”, “2. Support flow”) to route intents. Save/publish.

📸 Screenshot placeholder:
> [Screenshot: Absent Flow builder with option list]

### Step 3: Enable for absent/overflow
Assign this flow as the Absent Flow and ensure the absent/overflow condition is defined in channel settings.

📸 Screenshot placeholder:
> [Screenshot: Setting indicating Absent Flow assignment]

## What happens after it triggers?
Contacts get the absent message and can be routed to the options/flows you provide, keeping them engaged while your team is unavailable.

## Important behavior to know
- Runs only under absent/overflow conditions.
- Options should map to valid flows so contacts aren’t stuck.

## Common issues & solutions
- Not firing: check the overflow/absent condition and that the flow is assigned.
- Options not working: verify each option points to a live flow.

## Best practice 💡
- Offer 2–4 clear options; avoid long menus.
- Include expected response time or follow-up promise to set expectations.
