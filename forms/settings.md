# Forms: Settings & SEO

## Configuring Your Form (Step 2)
The **Form Settings** tab is where you control how the form behaves and how responses are delivered.

### General Settings
- **Form Name**: The internal name for your reference.
- **Form Link (Slug)**: Customize the URL of your form (e.g., `luluchat.io/team/my-survey`).
- **Is Publish**: Toggle this to make the form live or take it offline.

### Verification & Delivery
- **OTP Verification**: If enabled, unidentified recipients must verify their phone number via a WhatsApp OTP code before submitting. This ensures high-quality, verified data.
- **Delivery Logic**: Choose how you want to deliver form responses to the customer via WhatsApp:
    - **Do not send**: Only you see the responses.
    - **Send to all**: Everyone gets a copy of their answers.
    - **Send only to verified**: Only users who passed OTP or came via a Message Flow get a copy.

### Automated Responses
You can customize the confirmation message customers receive after submitting.
- Use placeholders like `{{1}}`, `{{2}}`, etc., to reference the answers they just provided.

📸 Screenshot placeholder:
> [Screenshot: Form settings page showing the OTP toggle and message template box]

### SEO & Sharing
Customize how your form looks when shared on social media or WhatsApp:
- **Meta Title & Description**: The text that appears in the link preview.
- **Meta Image**: Upload a brand logo or promotional banner for the link preview.

## Important behavior to know
- **OTP for External Links**: OTP is mostly needed for forms shared as public links. If a user enters a form through an automated **Message Flow**, they are already verified, and OTP is skipped.
