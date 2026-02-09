# Webhook Trigger

You need to create a message flow in Luluchat.io platform and configure webhook trigger in the said message flow. Then you will get the flow UUID to fulfil this webhook call.

The message flow webhook trigger must be triggered by HTTP POST method and "contact\_number" is compulsory in POST body parameter in order to trigger to send the message flow to the contact.

You may include other POST body parameters to send to trigger webhook to preset custom attribute for the said contact. You may check "Data Formatting" to see supported value type to send in Overview section.

Details on how the webhook works can be found in our [postman documentation](https://documenter.getpostman.com/view/985588/2s93z9bMoA#03cb48c2-7df1-4aec-a418-8ff42982a984).

## **Prerequisites**

* You are required to create a message flow in Luluchat.io platform
* You are required to include Webhook Trigger as starting step in message flow.
* You are required to subscribe to Luluchat.io Pro plan to use this service.

https(
{

    url: "webhook url",
    method: "POST",
    data: {
        contact_number: "012312312",
        name: "john",
    }
}

)

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Create a Webhook Trigger in Message Flow

1. Go to **Message Flow** in the left menu
2. Create a new message flow or open an existing one
3. Add a **Webhook Trigger** as the starting step in your message flow
4. Configure the webhook trigger settings as needed

📸 Screenshot placeholder:

> \[Screenshot: Message Flow editor showing Webhook Trigger as starting step]
{% endstep %}

{% step %}
#### Customer End Integration

Integrate the webhook trigger from your customer's system by making an HTTP POST request to the webhook URL.

For detailed API documentation and examples, refer to our [Postman documentation](https://documenter.getpostman.com/view/985588/2s93z9bMoA#03cb48c2-7df1-4aec-a418-8ff42982a984).

**Example POST request:**
- **URL**: Your webhook URL (obtained from the message flow)
- **Method**: POST
- **Body**: JSON with `contact_number` (required) and other parameters

**Example JSON body:**
```json
{
  "contact_number": "012312312",
  "name": "John",
  "membership_tier": "Gold"
}
```

<figure><img src="../.gitbook/assets/Screenshot 2026-02-09 at 1.07.34 PM.png" alt=""><figcaption></figcaption></figure>

> \[Screenshot: Postman or API client showing POST request to webhook URL]
{% endstep %}

{% step %}
#### Data Mapping

When mapping data in your message flow, you can use the POST body parameters in two ways:

**Option 1: Direct usage in messages**
- Use `{{data.param_key}}` syntax directly in your message content
- Example: `{{data.membership_tier}}` will display the membership tier value from the POST body

**Option 2: Store in custom attributes**
- If you need to store the data in custom attributes for later use:
  1. In your message flow, add a step to set custom attributes
  2. Map the POST body parameter to the custom attribute
  3. Use `data.param_key` to reference the parameter value

📸 Screenshot placeholder:

> \[Screenshot: Message flow showing custom attribute configuration with data mapping from POST body parameters]

**Example:**
- POST body includes: `{ "contact_number": "012312312", "name": "John", "membership_tier": "Gold" }`
- In message: Use `{{data.name}}` to display "John" or `{{data.membership_tier}}` to display "Gold"
- In custom attribute: Map `data.membership_tier` to store the membership tier value
{% endstep %}
{% endstepper %}

## **Response**

* A successful response of HTTP status 200 will be returned
* An error response will be returned if compulsory field is not fulfilled.

{% hint style="warning" %}
Note for developer:

* This webhook expecting 1 level of body parameter ONLY. Any nested parameter will not be examined.
* Luluchat.io will validate the parameter-value sent in body, if the value isn't fulfils the requirement stated in [Data Formatting](/broken/pages/nfUbfeea4EzfUAG2evM2) section, Luluchat.io will **ignore / skip** the param to be set in custom attributes.
* There is rate limit applied in each of the webhook trigger. Maximum **60 requests** per minute.
{% endhint %}
