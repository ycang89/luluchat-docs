# AI Agent

## What is the AI Agent node?

The **AI Agent** node hands the conversation to an AI agent you created in **Minicrew AI** or **Praxus AI**. In the app: "An AI Agent will handle the conversation based on your uploaded documents." The agent chats with the contact, and the flow continues through one of four events: **Success**, **Escalate**, **Failed** or **No Reply**.

<figure><img src="../../.gitbook/assets/flow-node-ai-agent.png" alt="AI Agent (Minicrew) settings panel and node. The panel shows AI Agent set to Menu &#x26; Booking Bot and Event Handling: Event 1 Success linked to Anything Else Message, Event 2 Escalate and Event 3 Failed linked to Talk to Staff Message, and Event 4 No Reply with Timeout Duration 30 Minute linked to Still There Message. The node shows the agent name and description and the four event exits"><figcaption><p>An AI Agent node with all four events linked</p></figcaption></figure>

## When to use it?

* **Open questions**: Let customers ask about the menu, prices or opening hours in their own words.
* **Bookings and orders**: Let the agent guide the customer and then hand back to the flow.
* **Before your team steps in**: Let the agent answer first, and escalate to staff when needed.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Connect your AI provider

Connect **Minicrew AI** (or **Praxus AI**) in **Settings > Account > [Integration](../../settings/account/integration.md)**, and create your agent in that provider.
{% endstep %}

{% step %}
#### Add the node

In draft mode (click **Edit Flow**), click **+** (**Add Node**) and choose **Minicrew AI Agent** under **Content**. A node called **AI Agent (Minicrew)** is added. Click it to open the settings.

To send contacts here from a reply button, open the reply in a [Message](message.md) node and choose **Select Existing Step**, then pick this node.
{% endstep %}

{% step %}
#### Choose the agent

In **AI Agent**, choose your agent. Agents are grouped by provider (**Minicrew AI** and **Praxus AI**). Hover over the **i** icon to see an agent's description.

<figure><img src="../../.gitbook/assets/flow-node-ai-agent-select.png" alt="AI Agent dropdown open with the Minicrew AI group (Order Support Bot, Menu &#x26; Booking Bot selected) and the Praxus AI group (Refund Assistant)"><figcaption><p>Choosing an AI agent</p></figcaption></figure>
{% endstep %}

{% step %}
#### Set up Event Handling

Under **Event Handling**, click the button under each event and choose the next step (**Choose Next Step**):

| Event | When it happens |
| --- | --- |
| **Success** | When the objective is successfully fulfilled |
| **Escalate** | Require escalation to a human agent |
| **Failed** | Fallback steps of any failed situation |
| **No Reply** | Timeout if no reply for too long |

For **No Reply**, set the **Timeout Duration** and choose **Minute**, **Hour** or **Day**. The default is 30 minutes.
{% endstep %}

{% step %}
#### Publish

Check that every event is linked (unlinked events show in red on the node), then click **Publish Flow**.
{% endstep %}
{% endstepper %}

## What happens after it triggers?

* The selected agent takes over the conversation with the contact.
* When the agent finishes, the flow continues from the matching event: **Success**, **Escalate** or **Failed**.
* If the contact doesn't reply within the **Timeout Duration**, the flow continues from **No Reply**.
* The node has no **Next Step**. Only the four events lead onwards.

## Important behavior to know

* **Minicrew AI is required to add the node**: Without a Minicrew AI connection, **Minicrew AI Agent** is greyed out with "Integration with Minicrew is required".
* **Match the provider**: Nodes added from the menu are Minicrew AI steps. Choose an agent from the **Minicrew AI** group, otherwise the node can't show the agent's name.
* **Agents come from your provider**: The list is loaded from Minicrew AI and Praxus AI each time you open the node. Create or edit agents in the provider, not in Luluchat.

## Common issues & solutions

* **"No AI vendor API keys configured"**: No AI provider is connected. Connect Minicrew AI or Praxus AI in **Settings > Account > Integration**.

* **"Please create an AI Agent in Praxus AI or Minicrew AI"**: You are connected, but have no agents yet. Create one in your provider.
* **"Please choose AI Agent"** (shown in red on the node): No agent is selected. Click the node and choose one.
* **"Please enter Timeout Duration"**: Enter a number (1 or more) for **No Reply**.
* **Customers get stuck with the AI**: Make sure **Escalate**, **Failed** and **No Reply** all lead to a step, such as a message that tells them a staff member will reply.

<figure><img src="../../.gitbook/assets/flow-node-ai-agent-no-key.png" alt="AI Agent panel showing the red message No AI vendor API keys configured" width="400"><figcaption><p>The AI Agent panel when no AI provider is connected</p></figcaption></figure>

## Best practice 💡

* Link **Escalate** and **Failed** to a step that brings in your team, for example a message plus an **Add Assignee** action.
* Use **No Reply** to send a gentle reminder like "Are you still there? Reply *menu* whenever you are ready."
* Use normal Message nodes with reply buttons for simple yes/no choices, and the AI Agent for open questions.

## Related Documentation

* [Integration](../../settings/account/integration.md)
* [AI Settings](../../settings/tools/ai.md)
* [Message](message.md)
* [Actions](../logics/actions.md)
