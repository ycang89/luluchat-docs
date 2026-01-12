# Step: Trigger (Starting Step)

## What is the Trigger Step?
The Trigger (or Starting Step) is the most important node in any flow. it defines the "When" – the specific event or message that causes Luluchat to start this automation for a customer.

## Common Trigger Types
Depending on how you want to engage your customers, you can link various triggers to this step:
- **Keywords**: Starts when a customer types a specific word or phrase (e.g., "Price", "Hello").
- **Growth Tools**: Starts when a customer clicks a specific QR code, URL, or submits an embedded widget.
- **Web Widget**: Starts when a visitor interacts with your website's chat bubble.
- **Manual Trigger**: Can be sent manually by a team member from the `Inbox` or `Contacts` list.

## How to set it up (Step by Step)
1. Every new flow starts with a **Starting Step** already on the board.
2. Click on the node to open the configuration.
3. Use the **Add Trigger** button to define what activates this flow.
4. You can add multiple triggers to a single flow (e.g., the flow starts if the user types "Hi" OR clicks a specific QR code).

📸 Screenshot placeholder:
> [Screenshot: Starting Step configuration showing a Keyword trigger added]

## Important behavior to know
- **First Node**: The Starting Step is always the first node executed.
- **No Incoming Links**: This node cannot have arrows pointing *to* it; it only has an arrow pointing *from* it.
- **Trigger Limits**: Remember to check the [Flow Settings](../message-flows-editor.md) to control how often this trigger can fire for the same person.

## Best practice 💡
- **Use Clear Triggers**: Ensure your keywords are unique to avoid two different flows triggering at the same time.
- **Multiple Entry Points**: Link multiple Growth Tools to the same flow if you are running a campaign across different channels (e.g., Facebook and Instagram).
