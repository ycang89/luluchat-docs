# Webhook Action

Webhook Action is a message flow's feature that offer the ability to send notification or exchange data / information with third party platform using HTTP POST or HTTP GET method depends on what user has configured in Luluchat.io configuration.

## **Sending**

Luluchat.io will send a server HTTP call to the configured url in the message flow with the parameters below, they are sent in POST BODY or GET QUERYSTRING in first level method (No nesting parameters)

### **Sending parameters:**

For each HTTP call triggered by webhook action will at least consists the parameter below:

<table><thead><tr><th width="216">Parameter</th><th>Value</th></tr></thead><tbody><tr><td>contact_number</td><td><p>Contact number of the conversation.</p><p></p><p>Format: country prefix + phone number without symbols.</p><p>Example: 60123456789</p></td></tr><tr><td>name</td><td>Name of the contact associated with the conversation.</td></tr></tbody></table>

{% hint style="info" %}
User can set their own preferred parameters in message flow configuration to be sent in the same HTTP request.
{% endhint %}

## Receivin**g Response**

Luluchat.io will wait third party platform to reply response and proceed with the rest of message flow depend on the status of the response.

{% tabs %}
{% tab title="Success Response" %}
Any response returned with HTTP 2xx response code.
{% endtab %}

{% tab title="Error Response" %}
* Response other than HTTP 2xx response code (4xx, 5xx).
* Response Timeout.
{% endtab %}
{% endtabs %}

### **Processing Response Body**

Luluchat.io is expecting response body to be in JSON format ONLY (not others like XML, String, etc.).

In order for Luluchat.io to correctly store the returned data into custom attribute (configured in message flow), the response body must include all the set-able parameters in "data" field.

Consider the example below:

```json
{
    "data": {
        "param1": "value1",
        "numericParam": 1234,
        "dateParam": "2023-05-06"
    }
}
```

\{{data.param1\}}, \{{data.numericParam\}}, \{{data.dateParam\}} are make available to be save as custom attribute values.

{% hint style="warning" %}
Note for Developer:

* To minimising the response time for the conversation, Luluchat.io is expecting that the request should be responded in 10 seconds. (10 seconds timeout)
* The data that introduced to be save in custom attributes must follow the rules / format written in [Data Formatting](/broken/pages/nfUbfeea4EzfUAG2evM2) section
{% endhint %}
