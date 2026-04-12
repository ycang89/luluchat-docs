# WhatsApp Calling

## What is WhatsApp Calling?

WhatsApp Calling lets your business place and receive **voice calls** with customers on WhatsApp using Meta’s **Calling API**, connected to your **WhatsApp Business API (WABA / WhatsApp Cloud)** number.

In Luluchat, calls run in the **browser** (your microphone and speakers are used for audio). Meta sets the rules for **who may call whom**, **when**, and **how often**; your team uses Luluchat to start calls, answer inbound calls, and manage channel-level calling options.

{% hint style="info" %}
This feature is only available for **WhatsApp Cloud (WABA)** channels, not WhatsApp Personal.
{% endhint %}

## Who can use it (Meta eligibility)

To use Meta’s Calling API, your business must meet Meta’s **messaging tier** requirements. Help-center guidance commonly refers to a minimum of **2,000 business-initiated conversations** in a rolling **24-hour** period; Meta may update exact thresholds, so always confirm the latest rules in Meta’s documentation.

{% hint style="warning" %}
Eligibility and limits are defined by **Meta**, not Luluchat. If calling is unavailable or restricted, your WABA account may not yet meet Meta’s criteria, or regional rules may apply.
{% endhint %}

## How calling works in Luluchat

### Turn calling on for your channel

1. Open **Settings** and go to **Inbox** (URL: `/account/settings?view=inbox`).
2. Find **WhatsApp Cloud Calling Settings** (shown when the feature is enabled for your workspace).
3. Turn on **Is calling enabled?** and configure optional settings (see below).
4. Click **Save Call Settings**.

Optional settings in the same section:

* **Call Icon Visibility** — **Default** shows the call control in the chat header, or **Hide** if you do not want the icon shown.
* **Allow customers to request callback** — controls whether customers can request a callback (when enabled).
* **Define your business call hours** — timezone, weekly hours, and holiday ranges so expectations match when you accept calls.

📸 Screenshot placeholder:

> \[Screenshot: Settings → Inbox → WhatsApp Cloud Calling Settings with “Is calling enabled?” and related fields]

### Request permission and place or receive a call

Meta requires **the contact’s permission** before your business can place an outbound call.

**In the inbox (WABA channel, one-to-one chat):**

* If the customer **has not** granted call permission, use the **phone** control in the chat header. Luluchat opens **Request call permission**. Enter the short message that will be sent to the customer, then click **Send**.
* After permission is **granted**, the same control is used to **start a call** (tooltip: **Start call**).
* If permission is missing, trying to call may show a reminder to request permission first.

**Incoming calls:**

* When a customer calls your business, Luluchat can show an **Incoming WhatsApp Call** notification with **Accept** and **Reject**.
* During a call, a status area can show progress (for example ringing or in-call duration) and **End Call**.

<div><figure><img src="../.gitbook/assets/Screenshot 2026-04-12 at 6.10.10 PM.png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/Screenshot 2026-04-12 at 6.10.21 PM.png" alt=""><figcaption></figcaption></figure></div>

> \[Screenshot: WABA conversation header showing the phone icon for request permission / start call]

<figure><img src="../.gitbook/assets/Screenshot 2026-04-12 at 6.13.11 PM.png" alt=""><figcaption></figcaption></figure>

> \[Screenshot: Incoming WhatsApp Call notification with Accept and Reject]

Allow **microphone** access in the browser when prompted; without it, calls cannot connect.

## Meta rules: permissions and limits

### When you can ask for permission

* During an **open customer service window**, you may send a **free-form permission request**, or use a **call permission template** if the window is closed (template rules follow Meta’s messaging policies).

### Permission request frequency

* Up to **1 request every 24 hours**, and
* A maximum of **2 requests in 7 days**.

These limits **reset** when a **connected call** occurs between your business and that WhatsApp user (either direction), per common Meta/BSP documentation.

### If the contact approves or declines

* **Approved:** You may call **immediately** or anytime within **7 days** of approval.
* **Declined:** You must wait **24 hours** before sending another permission request.

### After permission is granted (call frequency)

* Up to **5 connected calls every 24 hours** to that contact (after they have granted permission).
* If **2 consecutive** outbound calls go **unanswered**, Meta’s experience may include a follow-up message to the contact about the granted permission.
* If **4 consecutive** outbound calls go **unanswered**, the **granted permission may be revoked automatically**. The contact can change permission later if they wish.

### User-initiated vs business-initiated calls

* A **user-initiated call** (customer calls you) does **not** automatically grant permission for **business-initiated** outbound calls. You still need to send a **permission request** before placing an outbound call, unless Meta’s product changes that rule.

### Where business-initiated calling may not be available

**Business-initiated** calling is not available in all countries. Help documentation often lists **business** numbers in these countries as **not** supporting business-initiated outbound calling: **United States, Canada, Egypt, Vietnam, and Nigeria**. **User-initiated** calls may still follow Cloud API regional availability.

Your **business WABA number’s country** must be in a **supported** region; the **customer’s** number can often be in any country where the Cloud API is available, subject to Meta’s rules.

## Technical limits (Calling API)

* The Calling API does **not** provide API access to **call recordings** or **transcriptions** through Meta’s standard offering.
* A single WhatsApp Business phone number can support large numbers of **concurrent** inbound and outbound calls (public documentation often cites on the order of **1,000 concurrent** inbound and **1,000 concurrent** outbound per number—confirm in Meta’s docs for current figures).

## Important behavior to know

* **Service window and templates:** Permission and templates follow Meta’s messaging rules; see [Service Window](service-window.md) for the 24-hour window in Luluchat.
* **Policies change:** Meta updates Calling API rules, regions, and tiers. Check Meta’s official Calling API / Cloud API documentation periodically.
* **Quality and blocks:** Unanswered calls and customer complaints can affect calling permission and account standing; follow the frequency and permission rules closely.

## Common issues & solutions

* **No phone icon in chat:** Confirm **WhatsApp Cloud Calling Settings** has **Is calling enabled?**, your channel is **WABA**, the chat is **not a group**, and your account has access to the calling feature.
* **“Request permission first” or call blocked:** Send a **permission request** and wait for approval; respect **decline** cooldowns and **24h / 7-day** request limits.
* **Call fails or no audio:** Check browser **microphone** permission, device input/output, and network; try another browser if WebRTC is blocked.
* **Business-initiated not allowed:** Your **business number’s country** may be in a region where Meta does not offer business-initiated calling; user-initiated flows may still apply.

## Best practice 💡

* Request call permission during active support conversations when a call genuinely helps the customer.
* Keep outbound attempts reasonable to avoid automatic **permission revocation** after repeated unanswered calls.
* Align **call hours** in **Settings → Inbox** with when your team can answer.
* For the 24-hour messaging window and templates, see [Service Window](service-window.md).

## References

* [Meta WhatsApp Business Platform / Cloud API documentation](https://developers.facebook.com/documentation/business-messaging/whatsapp/get-started) — authoritative source for eligibility, regions, and API updates.

## Related documentation

* [Service Window](service-window.md)
* [Connect WhatsApp Cloud (WABA)](../inbox/connect-whatsapp-cloud.md)
* [Inbox](../inbox/index.md)
