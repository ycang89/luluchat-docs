# Content: Start Flow

## What is the Start Flow Node?
The Start Flow node allows you to link one automation flow to another. This is essential for building modular and reusable automations.

## When to use it?
- **Reusable Components**: Create a "Main Menu" flow that links to several sub-flows.
- **Complexity Management**: Break a very long, complex journey into smaller, manageable flows.
- **Consistent Hand-offs**: Route customers from a promotional flow into a standard lead qualification flow.

## How to set it up (Step by Step)
1. In the Message Flow Editor, click **Add Node (+) > Content > Start Flow**.
2. Click the node to open the settings.
3. Select the target **Message Flow** you want to redirect the customer to.
4. When a contact reaches this node, they will exit the current flow and enter the starting step of the selected flow.

📸 Screenshot placeholder:
> [Screenshot: Start Flow node with a selection dropdown of available flows]

## Important behavior to know
- **One-Way Exit**: Once a customer enters a new flow via this node, they do not automatically return to the original flow unless you explicitly add another "Start Flow" node in the target flow.
- **Endless Loops**: Be careful not to link two flows back to each other in a way that creates an infinite loop.

## Best practice 💡
- **Standardize**: Create standard sub-flows for things like "Address Collection" or "Contact Support" so you don't have to rebuild them every time.
- **Modular Design**: Keep your primary flows focused on marketing/engagement and use sub-flows for detailed administrative tasks.
