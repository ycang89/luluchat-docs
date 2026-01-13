# Workflows

## What is Workflows?

Workflows let you run a chain of actions based on conditions and timing—ideal for structured follow-ups, routing, and scheduling beyond single-message replies.

## When does it trigger?

* When the workflow’s conditions are met (e.g., event-based or scheduled rules you configure).
* Only when the workflow is switched on.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Open Workflows

Go to `Automations` > `Workflows` to view existing workflows and their status.

📸 Screenshot placeholder:

> \[Screenshot: Workflows list with On/Off switches and Create Workflow button]
{% endstep %}

{% step %}
#### Create a workflow

Click `Create Workflow`, name it, and set the initial condition(s) that should start the workflow.

📸 Screenshot placeholder:

> \[Screenshot: Create Workflow form with name and condition setup]
{% endstep %}

{% step %}
#### Add actions and save

Add the actions the workflow should perform (e.g., send, route, tag, start a flow), then save.

📸 Screenshot placeholder:

> \[Screenshot: Workflow builder/listing showing actions configured]
{% endstep %}

{% step %}
#### Turn it on and test

Use the On/Off switch to activate the workflow, then trigger the condition in a test scenario to confirm it runs.

📸 Screenshot placeholder:

> \[Screenshot: Workflow list with the new workflow toggled On]
{% endstep %}
{% endstepper %}

## What happens after it triggers?

The workflow executes its actions in order—sending messages, routing, or updating records as configured—and records the latest status visible in the list.

## Important behavior to know

* A workflow must be On to run; Off pauses all actions.
* Conditions must be specific to avoid unintended triggers.
* Actions run in the order you configure; disabled steps are skipped.

## Common issues & solutions

* Nothing ran: ensure the workflow is On and the condition actually fired in the right channel or context.
* Partial actions: review the action order and required fields, then republish.
* Can’t find it: check permissions; some users may not see workflows.

## Example: Tracking New Leads

Here's a practical example of how to use workflows to automatically track new leads when they first contact you:

### Scenario
When a new contact messages your WhatsApp number for the first time, you want to automatically tag them as a "New Lead" or move them to a "Leads" inbox list for easy tracking and follow-up.

### Workflow Setup

{% stepper %}
{% step %}
#### Set the Trigger

1. Create a new workflow and name it "Track New Leads"
2. In "Choose how workflow starts", select **"When a New Contact comes in"**

This workflow will trigger automatically whenever someone messages your WhatsApp number for the first time.

📸 Screenshot placeholder:
> [Screenshot: Workflow creation form showing "When a New Contact comes in" selected]
{% endstep %}

{% step %}
#### Add an Action

Choose one of these actions to track the new lead:

**Option 1: Add a Tag**
1. Click "Add Action"
2. Select **"Add Tag"**
3. Choose the tag you want to apply (e.g., "New Lead", "Prospect", "Inquiry")
4. You can select multiple tags if needed

**Option 2: Move to Inbox List**
1. Click "Add Action"
2. Select **"Move to Inbox List"**
3. Choose the custom inbox list where you want to organize new leads (e.g., "Leads", "New Contacts", "Follow Up")

📸 Screenshot placeholder:
> [Screenshot: Workflow actions showing "Add Tag" and "Move to Inbox List" options]
{% endstep %}

{% step %}
#### Save and Activate

1. Click **"Save"** to save your workflow
2. Toggle the workflow **On** to activate it

The workflow is now active and will automatically run whenever a new contact messages you for the first time.

📸 Screenshot placeholder:
> [Screenshot: Workflow list showing "Track New Leads" workflow with toggle switched On]
{% endstep %}
{% endstepper %}

### What Happens

When a new contact messages your WhatsApp number:
1. The workflow automatically triggers
2. The contact is immediately tagged with "New Lead" (if you chose Option 1) or moved to your "Leads" inbox list (if you chose Option 2)
3. You can now easily find and filter new leads in your Contacts or Inbox

### Use Cases

* **Lead Qualification**: Automatically tag new contacts based on their inquiry type
* **Team Routing**: Move new leads to specific inbox lists for different team members to handle
* **Follow-up Reminders**: Combine with other workflows to send automated follow-up messages
* **Sales Pipeline**: Tag new leads and automatically assign them to your sales team

{% hint style="info" %}
**Tip**: You can combine both actions in the same workflow! Add both "Add Tag" and "Move to Inbox List" actions to organize new leads in multiple ways. Actions execute in the order you add them.
{% endhint %}

## Best practice 💡

* Keep names clear (purpose + trigger).
* Start with a narrow condition; broaden only after testing.
* Test with a small audience or test channel before full rollout.
* Use tags and inbox lists together to create a comprehensive lead tracking system.