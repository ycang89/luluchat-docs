# Starting & Complete Steps

## What are Starting & Complete Steps?

Every Message Flow begins with a **Starting Step** and usually ends with a **Complete Step**:

* **Starting Step**: The first step of the flow. Its **triggers** decide when the flow starts, for example when a customer sends a keyword, opens a WhatsApp link, or when a Shopify order is paid. Every flow has exactly one Starting Step.
* **Complete Step**: Marks the end of the flow. When a contact reaches it, the flow is finished for that contact.

In the editor's **Add Node** menu, both are under **Starting & Complete Step** as **Trigger** and **Complete**.

<figure><img src="../../.gitbook/assets/flow-complete-new-flow.png" alt="A new message flow in draft mode: Starting Step linked to Send Message 1, linked to Complete Step"><figcaption><p>A new flow starts with a Starting Step and ends with a Complete Step</p></figcaption></figure>

## When to use it?

* **Starting Step**: Set triggers whenever customers or other systems should start the flow on their own. Leave it without triggers if you only send the flow from a broadcast or another flow.
* **Complete Step**: Link the last step of each path to it, so every path has a clear ending.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Open your flow in draft mode

Go to **Automations** > **Message Flows**, open a flow, and click **Edit Flow**.
{% endstep %}

{% step %}
#### Add triggers to the Starting Step

Click the **Starting Step** and add one or more triggers, such as **Keyword** or **WhatsApp Link**. See [Trigger](trigger.md).

<figure><img src="../../.gitbook/assets/flow-trigger-buttons.png" alt="Trigger buttons: Keyword, WhatsApp Link, App Event, Webhook, Meta Ad, Deal Stage, Booking Event and Mention"><figcaption><p>Trigger types you can add</p></figcaption></figure>
{% endstep %}

{% step %}
#### End your paths at the Complete Step

Link the last step of each path to the **Complete Step**. See [Complete](complete.md).
{% endstep %}

{% step %}
#### Publish

Click **Publish Flow**. Triggers only work after you publish.
{% endstep %}
{% endstepper %}

## Steps in this Section

<table data-view="cards">
  <thead>
    <tr>
      <th></th>
      <th></th>
      <th data-hidden data-card-target data-type="content-ref"></th>
      <th data-hidden data-card-cover data-type="files"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Trigger (Starting Step)</strong></td>
      <td>Choose when the flow starts: Keyword, WhatsApp Link, App Event, Webhook, Meta Ad, Deal Stage, Booking Event or Mention</td>
      <td><a href="./trigger.md">./trigger.md</a></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Complete</strong></td>
      <td>Mark where the flow ends for a contact</td>
      <td><a href="./complete.md">./complete.md</a></td>
      <td></td>
    </tr>
  </tbody>
</table>

## Important behavior to know

* A flow has exactly one Starting Step. It can't be deleted, and no step can link into it.
* A flow can have only one Complete Step. It can't link to another step.
* Default Message and Away Message flows don't use triggers. They start based on their own rules.

## Best practice 💡

* Give each flow at least one trigger unless you only send it from broadcasts.
* End every path at the Complete Step so the flow reads clearly from left to right.

## Related Documentation

* [Trigger](trigger.md)
* [Complete](complete.md)
* [Message Flow Editor](../message-flows-editor.md)
* [Message Flows](../message-flows.md)
