# Smart Delay

## What is Smart Delay?
Smart Delay pauses a flow for a set time and then branches based on whether the contact replied (`answered`) or not (`not answered`).

## When does it trigger?
- When the flow reaches the `Smart Delay` step while the flow is active and the channel is connected.
- It watches for replies during the delay window.

## How to set it up (Step by Step)

### Step 1: Add a Smart Delay step
In `Automations` > `Message Flows`, open a flow and add a `Smart Delay` node from the Logic section.

📸 Screenshot placeholder:
> [Screenshot: Flow builder showing Smart Delay node added between steps]

### Step 2: Configure the delay
Set the duration (minutes/hours/days) and ensure the `answered` and `not answered` ports are connected to the next steps.

📸 Screenshot placeholder:
> [Screenshot: Smart Delay settings with duration and two response ports connected]

## What happens after it triggers?
- If the contact replies during the delay, the flow can follow the `answered` branch.
- If no reply arrives by the end of the delay, the flow follows the `not answered` branch.

## Important behavior to know
- Both branches should be connected to avoid stalls.
- The timer runs in real time; editing the flow after publishing does not change timers already in progress.
- Smart Delay is separate from `Delay`; it has reply-aware branching.

## Common issues & solutions
- Flow stopped: connect both `answered` and `not answered` ports.
- Reply ignored: verify the channel is connected and the delay window is long enough for a response.

## Best practice 💡
- Use Smart Delay after a prompt that expects a reply; send a gentle follow-up on the `not answered` path.
- Keep durations reasonable to avoid long queue times.
