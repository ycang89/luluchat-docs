# Opt In

## What is Opt In?
Marks the contact as opted in for messaging when this Action runs.

## When does it trigger?
- When the flow reaches this `Opt In` action while the flow is active and the channel is connected.

## How to set it up (Step by Step)

### Step 1: Open the flow and edit the Action node
In `Automations` > `Message Flows`, open a flow, select the `Action` step, and choose `Opt In`.

📸 Screenshot placeholder:
> [Screenshot: Action step showing the Opt In option]

### Step 2: Place it after consent
Add this action after the message where the contact grants consent, then save and publish.

📸 Screenshot placeholder:
> [Screenshot: Flow path showing Opt In action after a consent message]

## What happens after it triggers?
The contact’s opt-in status is set to allow messaging; the flow continues to the next step.

> [!NOTE]
> **Important behavior to know**
>
> - **Consent Required**: Contacts must have previously opted out before they can opt back in. You cannot opt in contacts who have never opted out.
> - **User Consent**: Use only when you have clear user consent. This action helps you comply with WhatsApp's messaging policies.
> - **Broadcast Eligibility**: Once a contact opts in, they become eligible to receive broadcasts again (assuming they meet other criteria like being imported to Contacts).
> - **Opt-in Status**: Opt-in status affects future messaging eligibility for broadcasts and automated flows.

## Common issues & solutions
- Status not updated: ensure the action is on the published path and the channel is connected.

## Best practice 💡
- Keep a clear consent prompt before this action.
- Tag or note the source of consent for compliance.
