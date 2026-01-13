# Message Flows

## What is Message Flows?
Message Flows let you design guided replies and routing paths. Use them as the response when a trigger fires (keywords, growth tools, widget, workflows) or as fallback flows (default/away/opt-in/out/absent) for handling contacts automatically.

## Message Flow Components
Message Flows are built using different types of nodes and steps:
- **[Message Flow Editor](./message-flows-editor.md)**: Learn how to use the visual flow builder
- **[Starting & Complete Steps](./steps/index.md)**: Configure how customers enter and exit flows
  - [Trigger](./steps/trigger.md): Set up entry points (Keyword, WhatsApp Link, App Event, Webhook)
  - [Complete](./steps/complete.md): Mark successful flow completion
- **[Content Nodes](./content-nodes/index.md)**: Add messaging and interactive experiences
  - [Message](./content-nodes/message.md): Send text, media, and quick-reply buttons
  - [Message Template](./content-nodes/message-template.md): Send official WABA templates
  - [Start Flow](./content-nodes/start-flow.md): Link to other flows for modular design
  - [Form](./content-nodes/form.md): Send forms to collect customer data
  - [AI Agent](./content-nodes/ai-agent.md): Handle open-ended inquiries with AI
- **[Logics](./logics/index.md)**: Control timing, branching, and background actions
  - [Actions](./logics/actions.md): Background tasks (tagging, assignment, webhooks)
  - [Round Robin](./logics/round-robin.md): Distribute traffic sequentially
  - [Smart Delay](./logics/smart-delay.md): Pause and branch based on replies
  - [Condition](./logics/condition.md): Create if/else branching logic
  - [Randomizer](./logics/randomizer.md): Split traffic randomly for A/B testing
- **[Fallback & Consent Flows](./default-flow.md)**: Default behaviors for your channel
  - [Default Flow](./default-flow.md): When no other flow matches
  - [Away Flow](./away-flow.md): When team is offline
  - [Absent Flow](./absent-flow.md): When no assignee is available
  - [Opt-In Flow](./opt-in-flow.md): When customer opts in
  - [Opt-Out Flow](./opt-out-flow.md): When customer opts out
- **[Actions Library](./actions/index.md)**: Complete reference of all available actions

## When does it trigger?
- When a linked trigger sends a contact into the flow (e.g., keyword match, growth tool entry, web widget, or workflow action).
- When a fallback flow (default, away, opt-in, opt-out, absent) is active for your channel and its condition is met.
- Only when the channel is connected and the flow is enabled.

## How to set it up (Step by Step)

### Step 1: Open Message Flows
Go to `Automations` > `Message Flows`. You’ll see the list plus `Create Message Flow` and `Create from template`.

📸 Screenshot placeholder:
> [Screenshot: Message Flows list showing the Create Message Flow button and Create from template link]

### Step 2: Create a flow
Select `Create Message Flow` to name your flow (or pick `Create from template` to start faster), then save to open the builder.

📸 Screenshot placeholder:
> [Screenshot: Create Message Flow modal with name field and Create action]

### Step 3: Build and save
In the flow builder, add steps and messages, then save/publish. If you need a fallback flow (away/absent/opt-in/out/default), configure its message and linked flows from the dedicated options.

📸 Screenshot placeholder:
> [Screenshot: Flow builder canvas with steps and a Save/Publish control]

### Step 4: Link a trigger
Attach the flow to a trigger (keyword, growth tool, web widget, or workflow action) so it starts automatically.

📸 Screenshot placeholder:
> [Screenshot: Trigger configuration showing a dropdown to select the flow to run]

## What happens after it triggers?
The flow starts immediately, sending each step in order, routing or tagging as configured, and moving the contact through the designed path.

## Important behavior to know
- Channel must be connected; otherwise flows won’t fire (you’ll see “Channel not connected”).
- Flows stay inactive until linked to a trigger or set as a fallback (default/away/opt-in/out/absent).
- Publishing saves the current version; drafts won’t run.
- Unique, clear flow names help when selecting from trigger dropdowns.

## Common issues & solutions
- Flow didn’t run: confirm the channel is connected and the flow is linked to a trigger.
- Wrong flow fired: check keyword/growth tool mappings and ensure fallbacks aren’t overriding.
- Contact stuck: review step order and conditions; publish changes after edits.
- Can’t find the flow in a trigger: make sure it’s saved and you have access to that channel.

## Best practice 💡
- Start from templates when available to save time.
- Keep names descriptive (purpose + audience).
- Test with a teammate or test contact before broad rollout.
- Use separate flows for different intents to keep logic simple.
