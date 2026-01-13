# Web Widget

## What is Web Widget?
The Web Widget lets visitors start a WhatsApp chat from your site. You can customize the button look, welcome content, and generate an embed code to add before the closing </body> on your pages.

## When does it trigger?
- When the widget is embedded on a page and a visitor clicks the chat button (or auto-open is on).
- Only after you generate and paste the code onto the site page(s).

## How to set it up (Step by Step)

{% stepper %}
{% step %}
### Open Web Widget

Go to `Automations` > `Web Widget` to open the widget setup page.

📸 Screenshot placeholder:
> [Screenshot: Web Widget page with Chat Button Settings and Generate Widget Code]
{% endstep %}

{% step %}
### Customize the chat button

Adjust button position, margins, color, border radius, and CTA text under `Chat Button Settings`. Use `Get Preview` to see how it looks.

📸 Screenshot placeholder:
> [Screenshot: Chat Button Settings panel showing color picker, position, CTA text, and Get Preview]
{% endstep %}

{% step %}
### Set brand and welcome text

Update brand name, subtitle, welcome message, and contact number in `Brand Setting`. Toggle `Open Widget by Default` if you want it to auto-open.

📸 Screenshot placeholder:
> [Screenshot: Brand Setting fields for name, subtitle, welcome text, and auto-open toggle]
{% endstep %}

{% step %}
### Generate and embed the code

Click `Generate Widget Code`, then copy the snippet and paste it before the closing </body> tag on every page where you want the widget to appear.

📸 Screenshot placeholder:
> [Screenshot: Generated code block with Copy button and instruction to place before </body>]
{% endstep %}
{% endstepper %}

## What happens after it triggers?
Visitors see your chat button, click it, and are sent into WhatsApp with your configured greeting and contact number, starting a conversation with your team.

## Important behavior to know
- The code must be placed on every page where you expect the widget to show.
- `Get Preview` helps you confirm styling before deploying.
- Auto-open affects first load; use it sparingly to avoid interrupting visitors.
- Updates require regenerating and re-embedding the latest code.

## Common issues & solutions
- Widget not showing: confirm the snippet is pasted before </body> on the live page and that caches/CDN are cleared.
- Wrong number or brand: update the fields, regenerate the code, and replace the snippet.
- Button overlaps content: adjust position/margins and preview again.

## Best practice 💡
- Match button color and copy to your site branding.
- Keep the welcome text short and action-oriented.
- Test on desktop and mobile pages to ensure placement is unobtrusive.
