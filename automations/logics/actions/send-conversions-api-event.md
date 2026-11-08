# Send Conversions API Event

{% hint style="warning" %}
**Temporarily unavailable**: The **Send Conversions API Event** button is currently hidden from the Action step, so you can't add this action to a flow right now. Actions that were added earlier still show in your flows and can still be opened and edited.
{% endhint %}

## What is Send Conversions API Event?

**Send Conversions API Event** is an action that reports a conversion, such as a **Purchase**, for the current contact to Meta through the Meta Conversions API (CAPI). The event is sent to a Meta dataset and shows up in Meta Events Manager and Ads Manager. This helps you see which ads turned into sales, and lets Meta optimise your campaigns on real results.

It works on **WhatsApp Business (WABA)**, **Messenger** and **Instagram** channels.

## When to use it?

* **Paid orders**: Report a **Purchase** with the order value when a customer pays for a catering order.
* **Qualified leads**: Report a **QualifiedLead** when a customer asks for a quote.
* **Order updates**: Report **OrderShipped** or **OrderDelivered** as an order moves along.
* **Reviews**: Report **RatingProvided** or **ReviewProvided** after a feedback flow.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Open the action

In **Automations** > **Message Flows**, open the flow and click **Edit Flow**. Click the Action step that holds the **Send Conversions API Event** card, then click the card to open its settings.
{% endstep %}

{% step %}
#### Choose the dataset and event

* **Dataset** (required): The Meta dataset that receives the event, shown as name and ID. A new action picks the channel's first dataset for you. If a dataset you just created in Meta is missing, click the reload button (**Reload datasets from Meta**) next to the field.
* **No dataset yet?** If the channel has no dataset on Meta, the window only shows a **Dataset name** box and **Create Dataset**, so you set this up first. The name is filled in as the platform and your channel name, e.g. `WhatsApp - Kopi Corner`. Change it if you like, then click **Create Dataset**. Luluchat creates the dataset on Meta, selects it, and shows the rest of the settings.
* **Event** (required): The event to send. A new action starts on **Purchase**. The list is grouped into **Sales**, **Leads**, **Order updates** and **Feedback**, with a short hint under each event to help you pick. Events that need extra data say so, e.g. **Purchase (requires value, currency)**. See [Which event should I use?](#which-event-should-i-use) below.

<figure><img src="../../../.gitbook/assets/flow-capi-dataset-event.png" alt="Send Conversions API Event window with Dataset Messenger - Kopi Corner (880123456789012) selected and the Event list open under the Sales group, showing Purchase (requires value, currency) with the hint Payment confirmed. The strongest signal for Meta ads., then InitiateCheckout and AddToCart with their hints"><figcaption><p>A new action starts on the first dataset and Purchase. Each event has a hint to help you choose.</p></figcaption></figure>
{% endstep %}

{% step %}
#### Fill in Customer Information

Meta uses these details to match the event to a person. **Email** or **Phone Number** is required. The other fields help Meta find more matches.

| Field | Default | Tip |
| --- | --- | --- |
| **Email** | empty | Use a custom attribute that holds the email, e.g. `{{email}}` |
| **Phone Number** | `{{Contact No}}` | Keep the default for WhatsApp contacts |
| **Name** | `{{Full Name}}` | Keep the default |
| **City**, **State**, **Zip Code**, **Country** | empty | Type a value or use a custom attribute |

Click **{{}}** inside a field to insert contact details or custom attributes.
{% endstep %}

{% step %}
#### Add Custom Data

Custom data describes the conversion, such as the order value. Click **Add Parameter**, pick a **Parameter**, then enter its value. The value box changes with the parameter:

| Parameter type | Examples | How to enter it |
| --- | --- | --- |
| Number | `value`, `num_items`, `predicted_ltv` | A number, e.g. `1250.00`, or a placeholder |
| Currency | `currency` | A 3-letter code, e.g. `MYR` |
| Text | `content_name`, `order_id` | Free text or a placeholder |
| Choice | `content_type`, `delivery_category` | Pick from the list |
| True / False | `status` | Pick **True** or **False** |
| List | `content_ids` | Type a value and press Enter for each item |
| Item list | `contents` | Click **Add Item**, then fill in each item |

Parameters that the event needs are added for you, marked with `*`, and can't be removed.

<figure><img src="../../../.gitbook/assets/flow-capi-form.png" alt="Send Conversions API Event window for a Purchase: Customer Information with Email {{email}}, Phone Number {{Contact No}}, Name {{Full Name}}, City Kuala Lumpur and Country MY; Custom Data with value 1250.00, currency MYR and content_ids CAT-50PAX and PASTRY-SET"><figcaption><p>A Purchase event with customer details and custom data</p></figcaption></figure>
{% endstep %}

{% step %}
#### Save and publish

Click **Save**. The card turns green and shows the event, the dataset and the custom data being sent, e.g. "Send **Purchase** to **Kopi Corner WhatsApp**". Click **Publish Flow**.

<figure><img src="../../../.gitbook/assets/flow-capi-saved.png" alt="Action step Report Purchase to Meta with the Send Conversions API Event card reading Send Purchase to Kopi Corner WhatsApp, Custom data: value, currency, content_ids, shown in the side panel and on the canvas after a Payment Thanks message"><figcaption><p>The saved action</p></figcaption></figure>
{% endstep %}
{% endstepper %}

## Which event should I use?

Send the event at the moment the action happens in your flow, once per real action.

| Group | Event | Use it when the flow… | Needs |
| --- | --- | --- | --- |
| **Sales** | **Purchase** | confirms a paid order, e.g. after "Payment received, thank you" | `value`, `currency` |
| **Sales** | **InitiateCheckout** | sends a payment link or checkout | |
| **Sales** | **AddToCart** | records a product or service the customer picked | |
| **Sales** | **ViewContent** | shows a product, price list or catalogue | |
| **Sales** | **CartAbandoned** | follows up an unpaid cart or payment link | |
| **Leads** | **LeadSubmitted** | collects the contact's details, e.g. a booking or enquiry form | |
| **Leads** | **QualifiedLead** | marks the lead as a good fit, e.g. after your team qualifies it | |
| **Order updates** | **OrderCreated** | records the order, before payment | `value`, `currency` |
| **Order updates** | **OrderShipped** | tells the customer the order was sent out | `value`, `currency` |
| **Order updates** | **OrderDelivered**, **OrderCanceled**, **OrderReturned** | updates the customer on the order status | |
| **Feedback** | **RatingProvided**, **ReviewProvided** | receives a rating or a review from the contact | |

* **Selling products?** Send **Purchase** when payment is confirmed. It is the strongest signal for Meta ads.
* **Taking bookings or enquiries?** Send **LeadSubmitted**, then **QualifiedLead** once the lead is confirmed.
* **ViewContent**, **AddToCart** and **InitiateCheckout** are optional. Use them if you want to see the steps before a purchase in Events Manager.

## What happens after it triggers?

* Luluchat sends the event to the selected dataset for the current contact. Placeholders are filled in with the contact's details.
* The event appears in Meta Events Manager and Ads Manager.
* The flow continues to the next step.

## Important behavior to know

* **WhatsApp Business needs an ad click**: On WABA channels, the event is only sent if the contact messaged you from a Click-to-WhatsApp ad in the last 7 days. Otherwise it is skipped.
* **7-day window**: Meta only accepts events within 7 days of the contact's conversation.
* **Datasets**: Each channel sends events to the dataset linked to its WhatsApp Business Account, Facebook Page or Instagram account in Meta. You can create it from this window with **Create Dataset**, or in Meta Events Manager. **Create Dataset** only appears while the channel has no dataset yet.
* **One dataset per platform**: A dataset created here belongs to that channel's account only. Your WhatsApp, Messenger and Instagram channels each get their own, unless you connect one dataset to all of them in Meta Business settings.
* **Empty rows are skipped**: Custom Data rows left empty are not sent.
* **One per Action step**: You can't add this action twice in the same Action step. Use another Action step to send a second event.
* **Not on WhatsApp channels**: The action is not available on WhatsApp (non-WABA) channels.

## Common issues & solutions

* **I can't find the button**: The action is temporarily hidden. See the note at the top of this page.
* **"Please select a dataset."** or **"Please select an event."**: Choose both before you click **Save**.
* **"Email or phone number is required."**: Fill in **Email** or **Phone Number**. Keep `{{Contact No}}` in **Phone Number** for WhatsApp contacts.
* **"Purchase requires: value, currency"**: Add the missing Custom Data parameters and give them values.
* **The card says "Please provide the customer's email or phone number."**: Open the action and fill in **Email** or **Phone Number**.
* **I only see Create Dataset**: The channel has no dataset on Meta yet. Click **Create Dataset** to make one. If you created one in Meta Events Manager instead, click the reload button next to it.
* **"Your access token does not have permission to manage conversion events"**: Reconnect the channel to grant Luluchat the permission, then try **Create Dataset** again.
* **Events don't appear in Ads Manager**: The contact didn't come from a Click-to-WhatsApp ad in the last 7 days (WABA), or the conversation is older than 7 days.

## Best practice 💡

* Send **Purchase** with an accurate `value` and `currency`. It gives Meta the strongest signal.
* Already use a dataset for your website or another channel? Connect it to this channel's account in Meta Business settings and click the reload button, instead of creating a new one. One shared dataset gives Meta more data to learn from.
* Fill in as many Customer Information fields as you have data for, to raise Meta's match rate.
* Place the action in flows that run soon after the customer chats with you, such as right after payment is confirmed.

## Related Documentation

* [Trigger](../../steps/trigger.md)
* [Deals](../../../deals/index.md)
* [Logic: Actions](../actions.md)
