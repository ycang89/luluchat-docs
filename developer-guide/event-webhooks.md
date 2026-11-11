# Event Webhooks

## What are Event Webhooks?

Event Webhooks let Luluchat notify your system when something changes, for example when a contact is created, updated or tagged, or when a message is sent or received. Instead of asking the API for changes over and over, you give Luluchat a URL and it sends a `POST` request to that URL as soon as the event happens.

Use it to keep a CRM, database or spreadsheet in sync with your Luluchat contacts, or to copy chat messages into your own system.

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
| `message.all` | A contact sends a message, your team sends one, or an Open API send fails. Works on WhatsApp, WhatsApp Cloud (WABA), Messenger and Instagram channels. See [Message events](#message-events). |

## Prerequisites

* **Event Webhook enabled for your team.** It is off by default. Check `Settings` > `Account` > `Integration` > **Event Webhook**: it shows *Event webhook is enabled* when it's on. Otherwise, contact Luluchat support to enable it.
* **An access token with All Event Webhook Scopes.** See [Open API: Create an access token](open-api.md#step-1-create-an-access-token).
* **A public HTTPS URL** on your server that accepts `POST` requests with a JSON body.

## Endpoints

All endpoints use the [Open API](open-api.md) base URL `https://open-api.luluchat.io/v1/` and your access token in the `Authorization: Bearer ...` header.

| Method | Path | Scope | Description |
| --- | --- | --- | --- |
| `GET` | `/event-webhooks/available-events` | `api:event-webhook:read` | [List events you can subscribe to](#optional-check-the-available-events) |
| `POST` | `/event-webhooks/register` | `api:event-webhook:write` | [Subscribe a URL to an event](#register-the-webhook) |
| `GET` | `/event-webhooks/registered` | `api:event-webhook:read` | [List your subscriptions and signing secret](#list-registered-webhooks) |
| `POST` | `/event-webhooks/remove` | `api:event-webhook:write` | [Unsubscribe from an event](#remove-a-webhook) |
| `POST` | `/event-webhooks/reset-signing-secret` | `api:event-webhook:write` | [Create a new signing secret](#reset-the-signing-secret) |

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

Make a change in Luluchat, e.g. add a tag to a test contact for `contact.tag-updated`, or send a message to your channel for `message.all`. Your URL should receive a request within a few seconds.
{% endstep %}
{% endstepper %}

## What your server receives

Luluchat sends a `POST` request with these headers:

```
Content-Type: application/json
X-Webhook-Signature: sha256=5d41402abc4b2a76b9719d911017c592...
```

The JSON body always has `event`, `occurred_at` and `data`. What's in `data` depends on the event.

### Contact events

For the four `contact.*` events, `data` is the full contact:

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

### Message events

One subscription, `message.all`, sends every message on your channels. Register it like any other event (`"event": "message.all"`). `data.type` tells you what happened:

| `data.type` | Sent when |
| --- | --- |
| `message.received` | A contact sends a message |
| `message.sent` | Your team sends a message: from the Luluchat inbox, an automation, workflow, broadcast, AI agent, form, integration or the [Open API](open-api.md), or directly from the phone (WhatsApp) or the Meta inbox (Messenger / Instagram) |
| `message.failed` | A message you sent through the [Open API](open-api.md) did not go out |

{% hint style="info" %}
You can't subscribe to `message.received`, `message.sent` or `message.failed` on their own. Register `message.all` and check `data.type`.
{% endhint %}

```json
{
  "event": "message.all",
  "occurred_at": "2026-11-11T08:15:02.114Z",
  "data": {
    "type": "message.received",
    "changes": [
      {
        "chat_id": "60123456789@s.whatsapp.net",
        "message": {
          "id": "3EB0A1B2C3D4E5F6",
          "type": "text",
          "text": "Hi, is the 3pm slot still available?",
          "sent_at": "2026-11-11T08:15:00Z",
          "quoted": null,
          "ad": null,
          "link": null,
          "media": null,
          "location": null,
          "contacts": null,
          "reaction": null,
          "selection": null,
          "product": null,
          "interactive": null,
          "error": null
        },
        "contact": {
          "id": 10452,
          "name": "Jason Tan",
          "display_name": "Jason Tan",
          "push_name": "Jason",
          "username": "",
          "iso_contact_number": "+60123456789"
        },
        "sender": {
          "chat_id": "60123456789@s.whatsapp.net",
          "name": "Jason",
          "display_name": "Jason Tan",
          "username": ""
        },
        "sent_by": null,
        "reference": null,
        "channel": {
          "uuid": "3f6c2a1e-8b7d-4c5e-9a10-2b3c4d5e6f70",
          "type": "whatsapp",
          "contact_number": "60198765432"
        }
      }
    ]
  }
}
```

Each request carries one message in `data.changes`. Its fields:

| Field | Description |
| --- | --- |
| `chat_id` | The chat the message belongs to. Use it to reply. WhatsApp: `<number>@s.whatsapp.net`, or `<id>@g.us` for a group. Messenger: `<id>@fb`. Instagram: `<id>@ig`. |
| `message` | The message itself. See below. |
| `contact` | The chat's contact: `id`, `name`, `display_name`, `push_name`, `username`, `iso_contact_number`. In a group, this is the group. `null` if the contact didn't exist yet when the event was sent (a brand-new contact's first message). |
| `sender` | Who wrote the message: `chat_id`, `name`, `display_name`, `username`. In a group, this is the member who wrote it. For `message.sent`, it's your channel. |
| `sent_by` | `null` for `message.received`. For `message.sent`: `{ "source", "name" }`, see below. |
| `reference` | For a message sent through the Open API: the `reference` you passed, or the one the send response gave you. Use it to match the event to your send. `null` otherwise. |
| `channel` | `uuid`, `type` (`whatsapp`, `waba`, `messenger` or `instagram`) and `contact_number` (the channel's number; the Page ID on Messenger, the Instagram account ID on Instagram). |

#### The `message` object

Every key is always present, and is `null` when it doesn't apply to the message type.

| Key | Description |
| --- | --- |
| `id` | Message ID. Use it to ignore duplicates. |
| `type` | `text`, `image`, `video`, `audio`, `document`, `sticker`, `location`, `contacts`, `reaction`, `button_reply`, `list_reply`, `product`, `interactive` or `unsupported` |
| `text` | The text, or the caption of a media message |
| `sent_at` | When the message was sent (UTC) |
| `quoted` | The message this one replies to: `message_id`, `from_me`, `type`, `text`, plus `media` / `location` / `contacts` / `product` when the original has them. If the original isn't stored in Luluchat, only `message_id` is filled. |
| `ad` | Set when the chat came from a click-to-WhatsApp, click-to-Messenger or click-to-Instagram ad: `source_type`, `source_id`, `source_url`, `headline`, `body`, `media_type`, `media_url`, `thumbnail_url`, `ctwa_clid` |
| `link` | Messenger / Instagram only: a shared post or link card, `{ "url", "title" }` |
| `media` | `image`, `video`, `audio`, `document`, `sticker`: `{ "url", "mime_type", "filename" }` |
| `location` | `{ "latitude", "longitude", "name", "address" }` |
| `contacts` | Shared contact cards: `[{ "name", "phones": [], "emails": [] }]` |
| `reaction` | `{ "emoji", "message_id" }`. `message_id` is the message reacted to. |
| `selection` | `button_reply`, `list_reply`: the option the contact picked, `{ "id", "title", "description" }` |
| `product` | `{ "id", "title", "description", "price": { "currency", "amount" }, "url" }` |
| `interactive` | A template or button message: `{ "header": { "type", "text", "media_url" }, "footer", "buttons": [{ "id", "title" }] }` |
| `error` | `unsupported` on WhatsApp Cloud (WABA): why Meta couldn't show the message, `{ "code", "title", "message", "details" }` |

#### Where a sent message came from (`sent_by.source`)

| `source` | `name` |
| --- | --- |
| `user` | The team member who sent it from the inbox |
| `workflow` | The workflow name |
| `open_api` | The access token name |
| `automation`, `broadcast`, `ai_agent`, `integration`, `form` | `null` |
| `phone` | `null`. Sent directly from the WhatsApp phone app. |
| `page_inbox` | `null`. Sent from the Facebook Page inbox, Meta Business Suite or the Instagram app. |

#### `message.failed`

Sent when a message you sent through the Open API didn't go out, or was skipped because an earlier message in the same request failed (`error.code` is then `skipped_previous_failed`). The change has `chat_id`, `contact`, `sent_by`, `reference` and `channel` as above, a short `message` (`{ "type", "text" }`) and an `error`:

```json
"error": {
  "code": "skipped_previous_failed",
  "message": "Not sent: an earlier message in the same request failed."
}
```

Use `reference` to match it to your send.

#### What is not sent

* Messages that failed to send, other than Open API sends (`message.failed` above)
* View-once messages, edits, deleted messages, calls and system notices
* WhatsApp status updates and channel (newsletter) posts

#### Messenger and Instagram

* `contact.iso_contact_number` is always `null`: these contacts have no phone number.
* `sender.name` is `null` for messages from the contact: Meta doesn't send a name.
* Photos or files sent together arrive as one event each. The first keeps Meta's message ID; the others get `.1`, `.2`, … added to it. A reply or ad is only on the first one.

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
* A retry sends exactly the same body, including `occurred_at`. To ignore duplicates, use `event` + `data.id` + `occurred_at` for contact events, and `message.id` (or `reference` for `message.failed`) for message events.
* Events are delivered in the background, so they may arrive slightly out of order. Use `data.meta.updated` to keep the newest contact, and `message.sent_at` to order messages.

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
| `channel_id` | No | Remove the webhook for this channel. Leave it out to remove the webhook for all channels; webhooks registered for a specific channel stay until you remove them with their `channel_id`. |

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
* **Message volume**: `message.all` sends every message in and out of your channels, including broadcasts. Make sure your server can keep up, or subscribe one channel only with `channel_id`.

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
