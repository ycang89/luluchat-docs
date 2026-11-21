# Group Message

## What is the Group Message node?

The **Group Message** node posts a WhatsApp message into one or more WhatsApp groups from your channel's number. It does **not** reply to the contact in the flow. Use it to share what the flow collected, such as a new lead's details, with a team group chat.

{% hint style="info" %}
**Group Message** is available on WhatsApp channels only. It does not appear in the **Add Node** menu on WhatsApp Business API, Messenger or Instagram channels.
{% endhint %}

## When to use it?

* **New leads to sales**: After an AI agent or a few questions collect the customer's name, phone and needs into custom attributes, post them to the "Sales Team" group.
* **Bookings to the outlet**: Tell the outlet's group chat that a customer just booked a table.
* **Escalations**: Alert the support group when a customer chooses "Talk to Staff".

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Add the node

In draft mode (click **Edit Flow**), click **+** (**Add Node**) and choose **Group Message** under **Content**. You can also drag a line from a step's output handle onto an empty part of the canvas and pick **Group Message** from the short menu.

The new node is named "Send Group Message". Its card has a red border until you set it up.
{% endstep %}

{% step %}
#### Choose the groups and write the message

Click the node, then click the **Send WhatsApp Group Message** card in the panel.

* **Group(s)**: Click the box and pick one or more groups. Type to **Search groups** by name. The list shows the WhatsApp groups your channel already has a chat with.
* **Message**: Type the message. Click **{{}}** (**Content Parameters**) next to the box to insert details of the contact going through the flow, such as `{{Full Name}}`, `{{Contact No}}` or a custom attribute, where your cursor is.

Click **Submit** to save.
{% endstep %}

{% step %}
#### Connect and publish

The card now reads "Will send "…" to" followed by your group names. Link the node to the next step if the flow should continue, then click **Publish Flow**.
{% endstep %}
{% endstepper %}

## What happens after it triggers?

Luluchat sends the message to each selected group from your channel's number, then moves on to the node's **Next Step**. If one group can't receive it, the others still get the message and the flow carries on.

## Important behavior to know

* **Parameters come from the contact in the flow**: `{{Full Name}}` and other parameters are filled with the details of the contact going through the flow, not the group's. A parameter with no value is sent blank.
* **Your number must still be in the group**: The message is sent from this channel's number. If the number left or was removed from a group, that group is skipped.
* **Only groups you've chatted in**: A group only appears in the list (and only receives the message) if your channel already has a chat with it.
* **It counts towards your message limit**: If your team has reached its plan's message limit, the group message is not sent.
* **Required fields**: You can't publish while a Group Message node has no group or no message. You'll see "The Group Message Node "…" is missing a group or message."

## Common issues & solutions

* **I can't see Group Message in the menu**: Switch to a WhatsApp channel. The node isn't available on other channel types.
* **My group isn't in the list**: Send or receive at least one message in that group from this channel first, then search again.
* **The group didn't get the message**: Check that your channel's number is still a member of the group and that the channel is connected.
* **A parameter came out empty**: The contact had no value for that attribute when the node ran. Make sure an earlier step saves it, for example with [Save to Attribute](../logics/actions/save-attribute.md).

## Best practice 💡

* Put the important details first, for example "New lead: {{Full Name}}, {{Contact No}}", so the team can read it at a glance.
* Use a dedicated group for flow alerts so they don't get lost in normal chat.
* To message a staff member privately instead of a group, use the [Send WhatsApp Message](../logics/actions/send-whatsapp-message.md) action.

## Related Documentation

* [Content Nodes](index.md)
* [Send WhatsApp Message](../logics/actions/send-whatsapp-message.md)
* [Save to Attribute](../logics/actions/save-attribute.md)
* [Message](message.md)
