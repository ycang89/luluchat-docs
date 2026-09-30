# Event Webhooks

## What are Event Webhooks?

Event Webhooks let Luluchat notify your system when something changes, for example when a contact is created, updated or tagged. Instead of asking the API for changes over and over, you give Luluchat a URL and it sends a `POST` request to that URL as soon as the event happens.

Use it to keep a CRM, database or spreadsheet in sync with your Luluchat contacts.

{% hint style="info" %}
Event Webhooks send data **out of** Luluchat. To start a message flow **from** your system, use the [Webhook Trigger](webhook-trigger.md) instead.
{% endhint %}

## Available events

| Event | Sent when |
| --- | --- |
| `contact.created` | A new contact is created |
| `contact.updated` | A contact is updated, including its assignee, subscription (opt-in/opt-out), collaborators or custom attributes |
| `contact.tag-updated` | Tags are added to or removed from a contact |
| `contact.list-updated` | A contact is added to or removed from a custom list (inbox tab) |

## Prerequisites

* **Event Webhook enabled for your team.** It is off by default. Check `Settings` > `Account` > `Integration` > **Event Webhook**: it shows *Event webhook is enabled* when it's on. Otherwise, contact Luluchat support to enable it.
* **An access token with All Event Webhook Scopes.** See [Open API: Create an access token](open-api.md#step-1-create-an-access-token).
* **A public HTTPS URL** on your server that accepts `POST` requests with a JSON body.

## How to register an event webhook (Step by Step)

All requests go to the [Open API](open-api.md) base URL `https://open-api.luluchat.io/v1/` with your token in the `Authorization` header.

{% stepper %}
{% step %}
#### Create an access token

Go to `Settings` > `Account` > [**Integration**](https://app.luluchat.io/settings?view=integration) > **Access Token** and click **Create Access Token**. Under **Scopes**, tick **All Event Webhook Scopes**. Copy the token.

{% hint style="warning" %}
Tick **All Event Webhook Scopes**, not only **Read / Write**. Read / Write alone can register webhooks but can't list them.
{% endhint %}
{% endstep %}

{% step %}
#### Prepare your webhook URL

Create an endpoint on your server, e.g. `https://example.com/luluchat/webhook`, that:

* accepts `POST` requests with a JSON body
* responds with a `2xx` status within **10 seconds**
* [verifies the signature](#verify-the-signature) of each request

{% hint style="success" %}
**Tip:** For a quick test, use a free request inspector such as [webhook.site](https://webhook.site) as your URL and watch the events arrive.
{% endhint %}
{% endstep %}

{% step %}
#### (Optional) Check the available events

```bash
curl https://open-api.luluchat.io/v1/event-webhooks/available-events \
  -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
  -H "Accept: application/json"
```

```json
{
  "status": true,
  "message": "OK",
  "data": [
    {
      "domain": "contact",
      "event": "contact.created",
      "description": "Triggered when a new contact is created."
    }
  ],
  "http_status": 200
}
```
{% endstep %}

{% step %}
#### (Optional) Get the channel ID

By default a webhook receives events from **all channels** in your team. To receive events from one channel only, get its `uuid` from [List Channels](open-api.md#list-channels).
{% endstep %}

{% step %}
#### Register the webhook

Send one request per event you want to receive:

```bash
curl -X POST https://open-api.luluchat.io/v1/event-webhooks/register \
  -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -d '{
    "event": "contact.updated",
    "webhook_url": "https://example.com/luluchat/webhook"
  }'
```

| Field | Required | Description |
| --- | --- | --- |
| `event` | Yes | The event name, e.g. `contact.updated` |
| `webhook_url` | Yes | Your URL, max 255 characters |
| `channel_id` | No | A channel `uuid` to receive events from that channel only. Leave it out for all channels. |

**Response:**

```json
{
  "status": true,
  "message": "OK",
  "data": {
    "event": {
      "event": "contact.updated",
      "channel_id": null,
      "webhook_url": "https://example.com/luluchat/webhook",
      "meta": {
        "created": "2026-09-30T02:15:00.000000Z",
        "updated": "2026-09-30T02:15:00.000000Z"
      }
    },
    "webhook_signing_secret": "Pr14mtqLQz461TqtdFbd3M2y..."
  },
  "http_status": 200
}
```
{% endstep %}

{% step %}
#### Save the signing secret

Store `webhook_signing_secret` securely on your server. You'll use it to [verify](#verify-the-signature) that requests really come from Luluchat. It's the same secret for all webhooks in your team.
{% endstep %}

{% step %}
#### Test it

Make a change in Luluchat, e.g. add a tag to a test contact for `contact.tag-updated`. Your URL should receive a request within a few seconds.
{% endstep %}
{% endstepper %}

## What your server receives

Luluchat sends a `POST` request with these headers:

```
Content-Type: application/json
X-Webhook-Signature: sha256=5d41402abc4b2a76b9719d911017c592...
```

and a JSON body with the event name, when it happened, and the full contact:

```json
{
  "event": "contact.updated",
  "occurred_at": "2026-09-30T02:20:11.482Z",
  "data": {
    "id": 10452,
    "name": "Jason Tan",
    "push_name": "Jason",
    "display_name": "Jason Tan",
    "type": "individual",
    "iso_contact_number": "+60123456789",
    "remarks": null,
    "is_unsubscribed": false,
    "is_ai_handling": false,
    "channel": {
      "uuid": "3f6c2a1e-8b7d-4c5e-9a10-2b3c4d5e6f70",
      "name": "Sales WhatsApp",
      "contact_number": "60198765432",
      "status": "ready",
      "type": "whatsapp",
      "is_instantiated": true,
      "meta": {
        "instantiated": "2026-01-15T03:20:11.000000Z",
        "created": "2026-01-15T03:18:42.000000Z",
        "updated": "2026-09-20T08:45:03.000000Z"
      }
    },
    "assignee": { "id": 12, "fullname": "Aisha Rahman" },
    "collaborators": [{ "id": 15, "fullname": "Daniel Wong" }],
    "tags": [{ "id": 88, "name": "VIP", "color": "#2f54eb" }],
    "list": [{ "id": 5, "name": "Follow Up", "color": "#fa8c16", "type": "custom" }],
    "attributes": [
      { "id": 31, "name": "membership_tier", "data_type": "string", "value": "Gold" }
    ],
    "meta": {
      "created": "2026-03-02T08:44:45.000000Z",
      "updated": "2026-09-30T02:20:11.000000Z"
    }
  }
}
```

All four contact events send the same `data` shape: the contact **as it is after the change**. Compare it with your own copy to see what changed.

## Verify the signature

Every request is signed so you can reject requests that don't come from Luluchat. The `X-Webhook-Signature` header is `sha256=` followed by the HMAC-SHA256 of the **raw request body**, using your signing secret as the key, in lowercase hex.

To verify:

1. Read the raw request body **before** parsing it as JSON.
2. Compute HMAC-SHA256 of the raw body with your signing secret.
3. Compare `sha256=<your result>` with the `X-Webhook-Signature` header using a constant-time comparison.
4. If they don't match, respond `401` and ignore the request.

{% tabs %}
{% tab title="Node.js (Express)" %}
```javascript
const crypto = require('crypto');
const express = require('express');
const app = express();

app.post('/luluchat/webhook', express.raw({ type: 'application/json' }), (req, res) => {
  const expected = 'sha256=' + crypto
    .createHmac('sha256', process.env.LULUCHAT_SIGNING_SECRET)
    .update(req.body) // raw Buffer
    .digest('hex');
  const received = req.get('X-Webhook-Signature') || '';

  if (expected.length !== received.length ||
      !crypto.timingSafeEqual(Buffer.from(expected), Buffer.from(received))) {
    return res.sendStatus(401);
  }

  const payload = JSON.parse(req.body);
  // Queue the work, then reply quickly
  res.sendStatus(200);
});
```
{% endtab %}

{% tab title="PHP" %}
```php
$body = file_get_contents('php://input');
$expected = 'sha256=' . hash_hmac('sha256', $body, getenv('LULUCHAT_SIGNING_SECRET'));
$received = $_SERVER['HTTP_X_WEBHOOK_SIGNATURE'] ?? '';

if (!hash_equals($expected, $received)) {
    http_response_code(401);
    exit;
}

$payload = json_decode($body, true);
// Queue the work, then reply quickly
http_response_code(200);
```
{% endtab %}

{% tab title="Python (Flask)" %}
```python
import hashlib, hmac, os
from flask import Flask, request, abort

app = Flask(__name__)

@app.post("/luluchat/webhook")
def luluchat_webhook():
    body = request.get_data()  # raw bytes
    expected = "sha256=" + hmac.new(
        os.environ["LULUCHAT_SIGNING_SECRET"].encode(), body, hashlib.sha256
    ).hexdigest()
    if not hmac.compare_digest(expected, request.headers.get("X-Webhook-Signature", "")):
        abort(401)

    payload = request.get_json()
    # Queue the work, then reply quickly
    return "", 200
```
{% endtab %}
{% endtabs %}

## Delivery and retries

* Luluchat waits up to **10 seconds** for your response.
* Any `2xx` response counts as delivered.
* If your server times out, can't be reached, or responds with another status, Luluchat retries **3 more times**: after 10 seconds, 30 seconds and 60 seconds. After that the event is dropped.
* A retry sends exactly the same body, including `occurred_at`. Use `event` + `data.id` + `occurred_at` to ignore duplicates.
* Events are delivered in the background, so they may arrive slightly out of order. Use `data.meta.updated` to keep the newest version.

## Manage your webhooks

### List registered webhooks

```bash
curl https://open-api.luluchat.io/v1/event-webhooks/registered \
  -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
  -H "Accept: application/json"
```

Returns all your subscriptions and your current `webhook_signing_secret`. `channel_id` is `null` for webhooks that receive events from all channels.

### Change a webhook URL

Register the same `event` (and `channel_id`, if you used one) again with the new `webhook_url`. Each event can have one URL for all channels, plus one URL per channel.

### Remove a webhook

```bash
curl -X POST https://open-api.luluchat.io/v1/event-webhooks/remove \
  -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -d '{ "event": "contact.updated" }'
```

| Field | Required | Description |
| --- | --- | --- |
| `event` | Yes | The event to unsubscribe from |
| `channel_id` | No | Only remove the webhook for this channel. Leave it out to remove **every** webhook for this event, including channel-specific ones. |

### Reset the signing secret

If your signing secret may have leaked, create a new one:

```bash
curl -X POST https://open-api.luluchat.io/v1/event-webhooks/reset-signing-secret \
  -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
  -H "Accept: application/json"
```

{% hint style="danger" %}
The old secret stops working immediately. Update your server with the new `webhook_signing_secret` from the response right away, or it will reject every event.
{% endhint %}

## Important behavior to know

* **Team scoped**: Webhooks only receive events for contacts in the team that owns the token.
* **Plan and subscription**: If Event Webhook is turned off or your subscription expires, no events are sent.
* **Bulk imports**: Importing contacts sends events for each contact whose custom lists change, so expect bursts during an import.

## Common issues & solutions

* **`Event webhook is not enabled for this team.`**: Contact Luluchat support to enable Event Webhook.
* **`Invalid Scope` when listing webhooks**: The token only has **Read / Write**. Create a token with **All Event Webhook Scopes**.
* **`Channel not found.`**: The `channel_id` isn't a channel `uuid` in your team. Get it from [List Channels](open-api.md#list-channels).
* **Nothing arrives**: Check that the URL is public and uses HTTPS, that it returns `2xx` within 10 seconds, and that the webhook shows up in [List registered webhooks](#list-registered-webhooks).
* **Signature never matches**: Make sure you hash the **raw** body, before any JSON parsing, and that you use the latest secret.

## Best practice 💡

* **Reply fast, work later**: Return `200` right away and process the event in a background job.
* **Always verify the signature** before trusting the data.
* **Handle duplicates**: Your endpoint may receive the same event more than once after a retry.
* **Subscribe only to what you need** to reduce traffic to your server.
