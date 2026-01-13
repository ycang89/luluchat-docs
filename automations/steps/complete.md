# Step: Complete

## What is the Complete Step?
The Complete node marks the successful end of a specific path within your flow. While not strictly required for a flow to function, it helps in organizing your diagram and tracking successful completions in your reports.

## When to use it?
- At the end of a lead qualification path to mark the contact as "Qualified".
- After a customer has successfully booked an appointment.
- When a support request has been fully resolved via automation.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
### Add the Complete Node

In the Message Flow Editor, click **Add Node (+) > Starting & Complete Step > Complete**.

📸 Screenshot placeholder:
> [Screenshot: Add Node menu with Starting & Complete Step > Complete highlighted]
{% endstep %}

{% step %}
### Connect to Your Flow

Connect the output of your final action or message to this node.

📸 Screenshot placeholder:
> [Screenshot: Flow diagram showing connection to Complete node]
{% endstep %}

{% step %}
### Customize the Title (Optional)

You can give the node a custom title (e.g., "Booking Finished") to make your reports easier to read.

📸 Screenshot placeholder:
> [Screenshot: Complete node at the end of a flow branch with custom title]
{% endstep %}
{% endstepper %}

## Important behavior to know
- **Dead End**: The Complete node has no output handles. It is the final stop for any contact who reaches it.
- **Reporting**: Using this node allows Luluchat to track "Completion Rates" for your automations, helping you see which flows are most effective.

## Best practice 💡
- **Use for Milestones**: Only place a Complete node when a customer has reached a meaningful goal in the conversation.
- **Clean Diagrams**: Use it to avoid having loose arrows at the end of your branches.
