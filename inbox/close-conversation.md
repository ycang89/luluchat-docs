# Close Conversation

## What is Close Conversation?
Closes the current thread in Inbox when you’re done, marking it as resolved while keeping the history.

## When does it trigger?
- When you click `Close` on an open conversation in Inbox.
- Available only if you have permission to close conversations.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
### Open the conversation
In `Inbox`, select the conversation you want to close.

📸 Screenshot placeholder:
> [Screenshot: Conversation thread open with action bar visible]
{% endstep %}

{% step %}
### Click Close
Use the `Close` action on the conversation toolbar to mark it resolved.

📸 Screenshot placeholder:
> [Screenshot: Close button highlighted on the action bar]
{% endstep %}

{% step %}
### Confirm status
The thread status updates to closed; it leaves open queues but remains searchable in history.

📸 Screenshot placeholder:
> [Screenshot: Conversation showing closed status indicator]
{% endstep %}
{% endstepper %}

## What happens after it triggers?
The conversation moves out of active views, stays in history, and any downstream automations that depend on open status stop for this thread.

## Important behavior to know
- Closing does not delete messages; it only changes status.
- If you add actions after closing in a flow, those actions still run unless removed.
- Reopening (if allowed) brings it back to active views.

## Common issues & solutions
- Cannot close: check your permissions or channel restrictions.
- Closed but still visible: you may be viewing filters that show closed threads; change the filter.

## Best practice 💡
- Send a brief wrap-up message before closing.
- Use tags before closing to aid reporting and search.
