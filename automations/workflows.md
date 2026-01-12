# Workflows

## What is Workflows?
Workflows let you run a chain of actions based on conditions and timing—ideal for structured follow-ups, routing, and scheduling beyond single-message replies.

## When does it trigger?
- When the workflow’s conditions are met (e.g., event-based or scheduled rules you configure).
- Only when the workflow is switched on.

## How to set it up (Step by Step)

### Step 1: Open Workflows
Go to `Automations` > `Workflows` to view existing workflows and their status.

📸 Screenshot placeholder:
> [Screenshot: Workflows list with On/Off switches and Create Workflow button]

### Step 2: Create a workflow
Click `Create Workflow`, name it, and set the initial condition(s) that should start the workflow.

📸 Screenshot placeholder:
> [Screenshot: Create Workflow form with name and condition setup]

### Step 3: Add actions and save
Add the actions the workflow should perform (e.g., send, route, tag, start a flow), then save.

📸 Screenshot placeholder:
> [Screenshot: Workflow builder/listing showing actions configured]

### Step 4: Turn it on and test
Use the On/Off switch to activate the workflow, then trigger the condition in a test scenario to confirm it runs.

📸 Screenshot placeholder:
> [Screenshot: Workflow list with the new workflow toggled On]

## What happens after it triggers?
The workflow executes its actions in order—sending messages, routing, or updating records as configured—and records the latest status visible in the list.

## Important behavior to know
- A workflow must be On to run; Off pauses all actions.
- Conditions must be specific to avoid unintended triggers.
- Actions run in the order you configure; disabled steps are skipped.

## Common issues & solutions
- Nothing ran: ensure the workflow is On and the condition actually fired in the right channel or context.
- Partial actions: review the action order and required fields, then republish.
- Can’t find it: check permissions; some users may not see workflows.

## Best practice 💡
- Keep names clear (purpose + trigger).
- Start with a narrow condition; broaden only after testing.
- Test with a small audience or test channel before full rollout.
