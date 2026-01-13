# Automations

## What is Automations?
Automations let you create hands-free replies and routing across message flows, keyword responses, growth entry points, multi-step workflows, and the web widget that captures visitors and directs them to the right path.

## When does it trigger?
- When a contact message matches a keyword you set under `Keywords`.
- When a visitor engages via the `Web Widget` entry point.
- When a `Growth Tool` entry point (e.g., embedded form/landing) is submitted.
- When a scheduled or event-based `Workflow` condition is met (such as new conversation or a defined time window).
- When a `Message Flow` is invoked by its configured trigger.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
### Open Automations
Open `Automations` from the left menu to see tabs for `Message Flows`, `Keywords`, `Growth Tools`, `Workflows`, and `Web Widget`.

📸 Screenshot placeholder:
> [Screenshot: Automations page showing tabs for Message Flows, Keywords, Growth Tools, Workflows, Web Widget]
{% endstep %}

{% step %}
### Choose an automation type
Select the tab you need (for example, `Message Flows`, `Keywords`, `Growth Tools`, `Workflows`, or `Web Widget`) and click its `Create` action (for flows you may see `Create Message Flow`; for workflows `Create Workflow`).

📸 Screenshot placeholder:
> [Screenshot: Selected Automations tab with the Create button visible]
{% endstep %}

{% step %}
### Configure trigger and actions
Set the trigger (keyword, entry point, schedule, or event), then define what should happen (auto-reply content, assign/route, add tags, move to channel, or start a flow). Include targeting such as channel, audience, or time window if available, then save.

📸 Screenshot placeholder:
> [Screenshot: Automation creation form showing trigger selection, action configuration, and save/publish controls]
{% endstep %}

{% step %}
### Publish and test
Enable or publish the automation, then test it in a low-traffic channel or with a test contact to confirm the trigger fires and the right action runs.

📸 Screenshot placeholder:
> [Screenshot: Automation list showing the new automation in enabled/active state]
{% endstep %}
{% endstepper %}

## Sections in Automations

- [Message Flows](./message-flows.md)
  - [Message Flow Editor](./message-flows-editor.md)
  - [Starting & Complete Steps](./steps/index.md)
    - [Trigger](./steps/trigger.md)
    - [Complete](./steps/complete.md)
  - [Content Nodes](./content-nodes/index.md)
    - [Message](./content-nodes/message.md)
    - [Message Template](./content-nodes/message-template.md)
    - [Start Flow](./content-nodes/start-flow.md)
    - [Form](./content-nodes/form.md)
    - [AI Agent](./content-nodes/ai-agent.md)
  - [Logics](./logics/index.md)
    - [Actions](./logics/actions.md)
    - [Round Robin](./logics/round-robin.md)
    - [Smart Delay](./logics/smart-delay.md)
    - [Condition](./logics/condition.md)
    - [Randomizer](./logics/randomizer.md)
  - Fallback & Consent Flows
    - [Default Flow](./default-flow.md)
    - [Away Flow](./away-flow.md)
    - [Absent Flow](./absent-flow.md)
    - [Opt-In Flow](./opt-in-flow.md)
    - [Opt-Out Flow](./opt-out-flow.md)
- [Keywords](./keywords.md)
- [Growth Tools](./growth-tools.md)
- [Workflows](./workflows.md)
- [Web Widget](./web-widget.md)

## What happens after it triggers?
The automation runs immediately with the defined actions: it sends the configured reply or flow, routes or assigns the conversation, applies tags or updates, and (where available) records the run in its log or history.

## Important behavior to know
- Automations must be enabled; drafts or disabled items will not run.
- Access controls apply: some tabs or actions stay hidden without the right permission.
- Keywords match the text you define; use distinct keywords to avoid overlaps.
- Workflows follow their configured step order; disabled steps are skipped.
- Web Widget and Growth Tools need to be embedded/published on the target page to trigger.

## Common issues & solutions
- Nothing happens: ensure the automation is enabled and the trigger (keyword, entry point, schedule) matches the test exactly.
- Wrong audience: review channel/audience/time filters and update them.
- Cannot find a tab: request access from an admin if your role hides it.
- Widget not firing: confirm the widget snippet is installed on the page and published.

## Best practice 💡
- Test new automations in a low-traffic channel or with a test contact before broad rollout.
- Keep names clear (purpose + audience) for easier maintenance.
- Use unique keywords to prevent conflicts.
- Review logs or histories after launch to fine-tune replies and routing.
