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

## What happens after it triggers?
- **Fixed Delay**: After the specified time period (minutes, hours, or days), the flow automatically continues to the next step.
- **Wait for Reply**: The flow pauses and waits for the customer to respond. Once they send any message, the flow continues on the "answered" path. If no reply arrives, it follows the "not answered" path after the delay period ends.

> [!NOTE]
> **Important behavior to know**
>
> - **Both Branches Required**: Both the "answered" and "not answered" branches should be connected to avoid stalls. If either path is missing, the flow will stall.
> - **Reply Detection**: In standard mode, any message from the customer (text, image, or media) counts as a reply. In strict mode, only specific interactions (like clicking a button or submitting a form) will trigger the "answered" path.
> - **24/7 Operation**: Delay timers run continuously, even during weekends or outside business hours. Messages will be sent when the timer expires, regardless of your team's working hours.
> - **Manual Override**: If you manually start a new flow for a contact who is currently waiting in a Smart Delay, the pending delay is automatically cleared to prevent conflicting messages.
> - **Real-Time Timers**: The timer runs in real time; editing the flow after publishing does not change timers already in progress.
> - **Separate from Delay**: Smart Delay is separate from the basic `Delay` action; it has reply-aware branching capabilities.

## Common issues & solutions
- **Flow stopped**: Ensure both the "answered" and "not answered" paths are connected to next steps. If either path is missing, the flow will stall.
- **Reply not detected**: Verify that your channel is connected and the delay window is long enough for the customer to respond. Check if you're using strict mode, which requires specific interactions.
- **User never replies**: If using "Wait for Reply", the flow will stay paused indefinitely if the customer doesn't respond. Consider using a fixed delay as a fallback or adding a Condition node later to check if a specific goal was reached.

## Best practice 💡
- Use Smart Delay after a prompt that expects a reply; send a gentle follow-up on the `not answered` path.
- Keep durations reasonable to avoid long queue times.
