# Round Robin

## What is Round Robin?

Round Robin is a distribution logic that ensures traffic or tasks are divided equally among multiple paths. It works by cycling through a list of "rounds" in order, starting again from the beginning once the last round is reached.

## When to use it?

* **Lead Distribution**: Equally distribute new leads among your sales team.
* **Support Load Balancing**: Ensure support tickets are shared fairly among agents.
* **Varied Responses**: Cycle through different message variations to keep content fresh.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Add the Round Robin Node

In the Message Flow Editor, click **Add Node (+) > Logics > Round Robin**.

📸 Screenshot placeholder:

> \[Screenshot: Add Node menu with Logics > Round Robin highlighted]
{% endstep %}

{% step %}
#### Configure Rounds

Click the node to open the configuration. Click **+ Add New Step** to create a new round (e.g., Round 1, Round 2, Round 3).

📸 Screenshot placeholder:

> \[Screenshot: Round Robin configuration drawer with the 'Add New Step' button]
{% endstep %}

{% step %}
#### Link Each Round

For each round, click **Choose Next Step** to link it to the desired path or teammate assignment.

📸 Screenshot placeholder:

> \[Screenshot: Round Robin node showing several rounds linked to different next steps]
{% endstep %}
{% endstepper %}

## What happens after it triggers?

The contact is automatically routed to the next round in sequence. The first contact goes to Round 1, the second to Round 2, and so on. Once all rounds have been used, it cycles back to Round 1.

{% hint style="info" %}
**Important behavior to know**

* **Sequential Cycling**: Round Robin cycles through rounds in strict order. If you have 3 rounds, the 4th contact will go to Round 1, the 5th to Round 2, and so on.
* **Persistent Memory**: The node remembers which round was last used, even if contacts arrive hours or days apart. This ensures fair distribution over time.
* **Re-ordering**: If you delete a round, the remaining rounds are automatically re-sequenced to maintain the cycle.
* **Dynamic Re-ordering**: If you change the order of rounds in the editor, the sequence is updated immediately for future contacts.
{% endhint %}

## Common issues & solutions

* **Uneven distribution**: Round Robin ensures equal distribution over time. If you notice one round getting more traffic, check that all rounds are properly linked and the flow is published.
* **Round deleted**: If you delete a round, the system automatically adjusts the sequence. Contacts will continue to be distributed evenly among the remaining rounds.

## Best practice 💡

* **Combine with Actions**: Link each round to an "Actions" node that assigns a different team member to ensure fair workload distribution.
* **Monitor Performance**: Regularly check if all paths in your Round Robin are performing as expected.
