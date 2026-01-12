# Message Flows

## What is Message Flows?
Message Flows let you design guided replies and routing paths. Use them as the response when a trigger fires (keywords, growth tools, widget, workflows) or as fallback flows (default/away/opt-in/out/absent) for handling contacts automatically.

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
