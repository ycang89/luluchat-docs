# Webhook Trigger

You need to create a message flow in Luluchat.io platform and configure webhook trigger in the said message flow. Then you will get the flow UUID to fulfil this webhook call.

The message flow webhook trigger must be triggered by HTTP POST method and "contact\_number" is compulsory in POST body parameter in order to trigger to send the message flow to the contact.

You may include other POST body parameters to send to trigger webhook to preset custom attribute for the said contact. You may check "Data Formatting" to see supported value type to send in Overview section.

Details on how the webhook works can be found in our [postman documentation](https://documenter.getpostman.com/view/985588/2s93z9bMoA#03cb48c2-7df1-4aec-a418-8ff42982a984).

## **Prerequisites**

* You are required to create a message flow in Luluchat.io platform
* You are required to include Webhook Trigger as starting step in message flow.
* You are required to subscribe to Luluchat.io Pro plan to use this service.

## **Response**

* A successful response of HTTP status 200 will be returned
* An error response will be returned if compulsory field is not fulfilled.

{% hint style="warning" %}
Note for developer:

* This webhook expecting 1 level of body parameter ONLY. Any nested parameter will not be examined.
* Luluchat.io will validate the parameter-value sent in body, if the value isn't fulfils the requirement stated in [Data Formatting](/broken/pages/nfUbfeea4EzfUAG2evM2) section, Luluchat.io will **ignore / skip** the param to be set in custom attributes.
* There is rate limit applied in each of the webhook trigger. Maximum **60 requests** per minute.
{% endhint %}

