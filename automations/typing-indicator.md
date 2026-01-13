# Typing Indicator

## What is Typing Indicator?

The Typing Indicator is a feature that makes your automated messages feel more natural and human-like. When enabled, it shows a "typing..." status in WhatsApp before your message is sent, simulating the experience of a real person typing a message.

## When does it trigger?

* When a Message node in your flow is configured with a typing wait time.
* Only if Typing Indicator is enabled in your Message Flows settings for your channel type (WhatsApp Personal or WhatsApp Cloud).
* The typing indicator appears before the message is sent, based on the configured wait time.

## How to set it up (Step by Step)

### Step 1: Enable Typing Indicator in Settings

Before you can use typing indicators in your message flows, you need to enable it globally:

{% stepper %}
{% step %}
#### Access Message Flows Settings

1. Go to `Settings` > `Tools` > `Message Flows`.
2. You'll see the "Typing Indicator Settings" section.

📸 Screenshot placeholder:
> [Screenshot: Message Flows settings page showing Typing Indicator section]
{% endstep %}

{% step %}
#### Enable for Your Channel Type

Toggle the appropriate switch based on your channel:

* **Enable Typing Indicator for WhatsApp Personal**: Toggle this "On" if you're using WhatsApp Personal channels.
* **Enable Typing Indicator for WhatsApp Cloud**: Toggle this "On" if you're using WhatsApp Business API (WABA) channels.

You can enable both if you use multiple channel types.

📸 Screenshot placeholder:
> [Screenshot: Typing Indicator toggles for Personal and Cloud]
{% endstep %}

{% step %}
#### Save Settings

Click **Save** to apply your changes. The typing indicator feature is now enabled for your message flows.

📸 Screenshot placeholder:
> [Screenshot: Save button in Message Flows settings]
{% endstep %}
{% endstepper %}

### Step 2: Configure Typing Indicator in Message Nodes

Once enabled in settings, you can configure typing wait time for individual Message nodes:

{% stepper %}
{% step %}
#### Open Your Message Flow

1. Go to `Automations` > `Message Flows`.
2. Open the flow you want to edit, or create a new one.
3. Add or select a **Message** node in your flow.

📸 Screenshot placeholder:
> [Screenshot: Message Flow editor with a Message node selected]
{% endstep %}

{% step %}
#### Configure Typing Wait Time

1. In the Message node, you'll see a clock icon (⏰) at the bottom right of each text content block.
2. Click the clock icon to open the typing indicator configuration.
3. Choose your typing wait time:
   * **Auto**: The system automatically calculates the wait time based on the message text length (recommended for natural feel).
   * **Custom (seconds)**: Set a fixed number of seconds (e.g., 2, 3, 5 seconds) for the typing indicator to show.

📸 Screenshot placeholder:
> [Screenshot: Message node showing clock icon and typing indicator dropdown with Auto and custom time options]
{% endstep %}

{% step %}
#### Save Your Flow

1. After configuring the typing wait time, save your Message node.
2. Save and publish your flow to apply the changes.

📸 Screenshot placeholder:
> [Screenshot: Save button in flow editor]
{% endstep %}
{% endstepper %}

## What happens after it triggers?

When a message flow runs with typing indicator enabled:

1. **Typing Indicator Shows**: Before the message is sent, WhatsApp displays a "typing..." indicator to the customer.
2. **Wait Time**: The system waits for the configured duration (Auto or custom seconds).
3. **Message Sends**: After the wait time, your message is delivered to the customer.
4. **Natural Experience**: The customer sees the typing indicator, making the automated message feel like it's coming from a real person.

## Typing Wait Time Modes

### Auto Mode

* **How it works**: The system automatically calculates the typing wait time based on the length of your message text.
* **When to use**: Recommended for most cases as it provides a natural, realistic typing experience.
* **Calculation**: Longer messages get longer wait times, shorter messages get shorter wait times.

### Custom Mode (Fixed Seconds)

* **How it works**: You set a fixed number of seconds (e.g., 2, 3, 5 seconds) for the typing indicator to show.
* **When to use**: When you want consistent timing regardless of message length, or when you want to create a specific pacing for your conversation flow.
* **Options**: Typically ranges from 1 to 10 seconds, depending on your configuration.

## Important behavior to know

* **Settings Required**: Typing indicator must be enabled in `Settings` > `Tools` > `Message Flows` before it will work in your flows. Enabling it in settings activates the feature globally for all message flows.
* **Per-Node Configuration**: Each Message node can have its own typing wait time configuration. You can use Auto for some messages and custom times for others.
* **Channel-Specific**: Typing indicator settings are separate for WhatsApp Personal and WhatsApp Cloud. Enable the one that matches your channel type.
* **Only for Message Nodes**: Typing indicator only applies to Message nodes, not Message Template nodes or other content types.
* **24-Hour Window**: Typing indicator works within the 24-hour service window. For messages outside this window (using templates), typing indicators may not apply.
* **Auto Calculation**: In Auto mode, the wait time is calculated based on text length. Very short messages may have minimal wait time, while longer messages will have proportionally longer wait times.
* **Visual Indicator**: The clock icon (⏰) in the Message node shows your current typing indicator setting. If disabled, it appears grayed out.

## Common issues & solutions

* **Typing indicator not showing**:
  * Check that Typing Indicator is enabled in `Settings` > `Tools` > `Message Flows` for your channel type (Personal or Cloud).
  * Verify that the Message node has a typing wait time configured (not set to disabled).
  * Ensure your flow is published and active.
  * Check that your channel is connected and in `ready` status.

* **Wait time too short or too long**:
  * If using Auto mode and the timing feels off, try switching to Custom mode and set a specific number of seconds.
  * Adjust the custom wait time to match your desired pacing (typically 2-5 seconds works well).

* **Clock icon not appearing**:
  * Ensure Typing Indicator is enabled in settings first.
  * Refresh the flow editor page.
  * Check that you're editing a Message node (not a Message Template node).

* **Different behavior for Personal vs Cloud**:
  * Remember that Personal and Cloud have separate typing indicator settings. Make sure you've enabled the correct one for your channel type.

## Best practice 💡

* **Use Auto Mode**: Auto mode provides the most natural typing experience as it adapts to message length automatically.
* **Test Your Timing**: Test your flows with typing indicators to ensure the wait time feels natural and not too slow or too fast.
* **Consistent Experience**: Consider using similar wait times across related messages in a flow for a consistent user experience.
* **Balance Speed and Natural Feel**: While longer wait times feel more natural, don't make customers wait too long. 2-5 seconds is usually optimal.
* **Enable for Both Channel Types**: If you use both WhatsApp Personal and WhatsApp Cloud, enable typing indicators for both in settings.

## Related Documentation

- [Message Node](content-nodes/message.md) - Learn how to create and configure Message nodes
- [Message Flows Settings](../settings/tools/message-flows.md) - Learn how to enable typing indicators globally
- [Message Flows Editor](message-flows-editor.md) - Learn how to use the flow builder
- [Message Flows Overview](message-flows.md) - Learn about message flows in general
