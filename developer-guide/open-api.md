# Open API

## What is the Open API?

The Luluchat Open API lets your own systems read data from your Luluchat workspace. For example, you can list your channels, check your team details, or look up the message flows you can trigger with a [Webhook Trigger](webhook-trigger.md).

Full request and response examples are in our [Postman documentation](https://documenter.getpostman.com/view/985588/2s9YJW4RAc).

{% hint style="info" %}
**Base URL**

```
https://open-api.luluchat.io/v1/
```

Every request must use HTTPS and include your access token.
{% endhint %}

## Prerequisites

* A Luluchat account with access to `Settings` > `Account` > `Integration`
* An **access token** with the right scopes (see below)

## Step 1: Create an access token

{% stepper %}
{% step %}
#### Open the Access Token section

Go to `Settings` > `Account` > [**Integration**](https://app.luluchat.io/settings?view=integration) and scroll to **Access Token**.
{% endstep %}

{% step %}
#### Click Create Access Token

Fill in the form:

* **Name**: Where the token is used, e.g. `CRM sync`
* **Expiry**: 1, 3, 6 or 12 months, or **Never**
* **Scopes**: Tick the scopes for the endpoints you need. See [Choosing scopes](#choosing-scopes).
{% endstep %}

{% step %}
#### Copy the token

Click **Submit**. Copy the token from the **Access Token Created Successfully** window and store it somewhere safe.

{% hint style="danger" %}
The token is **only shown once**. If you lose it, delete it and create a new one.
{% endhint %}
{% endstep %}
{% endstepper %}

### Choosing scopes

A token can only call the endpoints its scopes allow. Tick these options in the **Scopes** list:

| To use | Tick | Scope created |
| --- | --- | --- |
| [Get Team Profile](#get-team-profile) | **All Open API scopes** > **Team** | `api:team:*` |
| [List Message Flows](#list-message-flows) | **All Open API scopes** > **Message Flow** | `api:flow:*` |
| [List Channels](#list-channels) | **All Open API scopes** > **Channel** | `api:channel:*` |
| [Event Webhooks](event-webhooks.md) | **All Event Webhook Scopes** | `api:event-webhook:*` |

{% hint style="warning" %}
**Tick the group, not only "Read / Write".** A scope only allows what it names: **Read / Write** (`...:write`) lets you register and remove event webhooks, but **not** list them, which needs **Read Only** (`...:read`). Ticking the group (e.g. **All Event Webhook Scopes**) includes both.
{% endhint %}

## Step 2: Call the API

Send the token in the `Authorization` header of every request:

```
Authorization: Bearer YOUR_ACCESS_TOKEN
Accept: application/json
Content-Type: application/json
```

**Example: check that your token works**

```bash
curl https://open-api.luluchat.io/v1/teams/me \
  -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
  -H "Accept: application/json"
```

## Response format

Every response is JSON with the same wrapper:

```json
{
  "status": true,
  "message": "OK",
  "data": { },
  "http_status": 200
}
```

* `status` is `true` when the request succeeded.
* List endpoints also return `meta` with `page`, `pages`, `perpage` and `total`.

## Endpoints

| Method | Path | Scope | Description |
| --- | --- | --- | --- |
| `GET` | `/teams/me` | `api:team:read` | Get your team profile |
| `GET` | `/channels` | `api:channel:read` | List your channels |
| `GET` | `/automation-flows` | `api:flow:read` | List your message flows |
{% hint style="info" %}
Want Luluchat to notify your system when a contact changes? The Event Webhook endpoints use the same base URL and access token, and are documented in [Event Webhooks](event-webhooks.md).
{% endhint %}

### Get Team Profile

`GET /teams/me`

Returns the team (workspace) that owns the token. Useful to test your token.

```json
{
  "status": true,
  "message": "OK",
  "data": {
    "uuid": "0b6c6f0e-5a0e-4d7f-9a41-6a2f1f0d8c11",
    "name": "Kopi Corner",
    "status": "active",
    "meta": {
      "created": "2025-01-15T03:18:42.000000Z",
      "updated": "2026-09-20T08:45:03.000000Z"
    }
  },
  "http_status": 200
}
```

### List Channels

`GET /channels`

Lists your team's channels (deleted channels are not included). Use a channel's `uuid` as the `channel_id` when you [register an event webhook](event-webhooks.md) for one channel only.

| Query parameter | Description |
| --- | --- |
| `page` | Page number |
| `perpage` | Results per page (default 50), or `all` |
| `status` | Filter by status, e.g. `ready` |
| `name` | Filter by channel name |

```json
{
  "status": true,
  "message": "OK",
  "data": [
    {
      "uuid": "3f6c2a1e-8b7d-4c5e-9a10-2b3c4d5e6f70",
      "name": "Sales WhatsApp",
      "contact_number": "60123456789",
      "status": "ready",
      "type": "whatsapp",
      "is_instantiated": true,
      "meta": {
        "instantiated": "2026-01-15T03:20:11.000000Z",
        "created": "2026-01-15T03:18:42.000000Z",
        "updated": "2026-09-20T08:45:03.000000Z"
      }
    }
  ],
  "meta": { "page": 1, "pages": 1, "perpage": 50, "total": 1 },
  "http_status": 200
}
```

### List Message Flows

`GET /automation-flows`

Lists your message flows and flow templates, with the channel each belongs to. Use a flow's `uuid` with the [Webhook Trigger](webhook-trigger.md).

| Query parameter | Description |
| --- | --- |
| `status` | Filter by status, e.g. `active` |
| `page` | Page number |
| `perpage` | Results per page, or `all` |

```bash
curl "https://open-api.luluchat.io/v1/automation-flows?status=active" \
  -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
  -H "Accept: application/json"
```

## Errors

| Message | What it means | How to fix it |
| --- | --- | --- |
| `Invalid Access Token` | The token is missing, wrong, expired or deleted | Check the `Authorization: Bearer ...` header, or create a new token |
| `Invalid Scope` | The token doesn't have the scope this endpoint needs | Create a token with the right scope. See [Choosing scopes](#choosing-scopes). |
| `Channel not found.` | The `channel_id` doesn't belong to your team | Get the correct `uuid` from [List Channels](#list-channels) |

{% hint style="warning" %}
**Old API keys no longer work.** Authenticating with the team API key was deprecated on 31 March 2026. Use an access token instead.
{% endhint %}

## Best practice 💡

* **One token per integration**: Create a separate token for each system so you can revoke one without breaking the others.
* **Least privilege**: Only tick the scopes the integration needs.
* **Keep tokens secret**: Store tokens in environment variables or a secrets manager. Never put them in front-end code or a code repository.
* **Watch Last Used**: The Access Token table shows when each token was last used. Delete tokens that are no longer needed.
