# Logic: Condition

## What is the Condition Node?
The Condition node acts as an "If/Else" gateway. it checks specific criteria about a contact and splits the flow into different paths based on whether those conditions are met.

## When does it trigger?
This node triggers whenever a contact reaches it during a Message Flow. Luluchat instantly evaluates the defined rules against the contact's current data to decide which path to follow next.

## How to set it up (Step by Step)

<steps>
<step>
**Add the Node**

In the Message Flow Editor, click **Add Node (+) > Logics > Condition**.

📸 Screenshot placeholder:
> [Screenshot: Add Node menu with Logics > Condition highlighted]
</step>

<step>
**Define your Rules**

Click the node to open the conditions builder. Click **Add a Condition** to select your data source (e.g., Contact Tags, Custom Attribute, or Current Time).

📸 Screenshot placeholder:
> [Screenshot: Condition builder showing the 'Add a Condition' button]
</step>

<step>
**Choose Operator and Value**

Select how you want to compare the data (e.g., "includes", "is equal to", "is after") and enter the value to match against.

📸 Screenshot placeholder:
> [Screenshot: Operator and Value selection in the condition builder]
</step>

<step>
**Link your Paths**

Define the **Next Step** for when the condition is met (Matched) and a **Fallback Step** (Else) for when it is not.

📸 Screenshot placeholder:
> [Screenshot: Condition node on the board with Matched and Else paths linked to other nodes]
</step>
</steps>

## What happens after it triggers?
The contact is immediately routed to the next step in the "Matched" path if the rules are true, or the "Else" path if they are not. This happens silently in the background without the customer seeing any "processing" state.

{% hint style="info" %}
**Important behavior to know**

- **First Match Wins**: If you have multiple condition sets, Luluchat checks them in order and follows the first one that matches.
- **The "Else" Path**: Always ensure you have a default path for contacts who don't meet any of your specific conditions to prevent the flow from getting stuck.
- **Real-Time Data**: Luluchat uses the most up-to-date information from the contact's profile at the exact moment they reach the node.
- **Case Insensitive**: Text comparisons (like Tag names) are generally case-insensitive.
- **Contact Activity Context**: When checking "Last Conversed", "Last Contact Replied", or "Last Replied From You", remember that "you" represents the channel, not the individual team member.
{% endhint %}

## Common issues & solutions
- **Wrong Path Taken**: Check the order of your conditions. If a broad rule is above a specific one, the broad rule will capture the contact first.
- **Empty Fields**: If you are checking a Custom Attribute that hasn't been filled yet, use the "is unknown" operator to handle those contacts.
- **Case Sensitivity**: Text comparisons (like Tag names) are generally case-insensitive.

## Best practice 💡
- **Weekend Routing**: Use the **Occurrence Date** field with the **is on** operator to send different automated replies during the weekend.
- **Personalized Journeys**: Use conditions early in a flow to check for a "VIP" tag and offer a more personalized experience to your best customers.
