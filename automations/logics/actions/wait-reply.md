# Wait for Reply

## What is Wait for Reply?
Holds the flow for a set time while waiting for the contact to respond; if no reply arrives, it follows the “not answered” path.

## When does it trigger?
- When the flow reaches this `Wait for Reply` action while the flow is active and the channel is connected.
- It watches for any incoming reply during the wait window.

## How to set it up (Step by Step)

### Step 1: Open the flow and edit the Action node
In `Automations` > `Message Flows`, open a flow, select the `Action` step, and choose `Wait for Reply`.

📸 Screenshot placeholder:
> [Screenshot: Action step showing the Wait for Reply option]

### Step 2: Set the wait window
Enter how long to wait (minutes/hours) and connect the “not answered” path to a follow-up step.

📸 Screenshot placeholder:
> [Screenshot: Wait for Reply action form with duration and response path]

## What happens after it triggers?
- If the contact replies within the window, the flow can proceed from the incoming message context.
- If no reply arrives, the flow follows the “not answered” branch you connect.

## Important behavior to know
- The timer counts real time; pausing or leaving the page does not stop it.
- Ensure the “not answered” path is connected to avoid stalls.

## Common issues & solutions
- Flow stalled: connect the “not answered” port to a next step.
- Reply missed: verify the wait duration is long enough and the channel is connected.

## Best practice 💡
- Keep the wait window short for quick follow-ups; send a gentle reminder on the “not answered” path.
