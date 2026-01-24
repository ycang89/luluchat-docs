## Setup WABA Message Template for Form Response

This guide shows you how to:

- Create a WhatsApp Business (WABA) message template in Meta's WhatsApp Manager for form responses.
- Configure your Luluchat form to send this template to the submitter, including a dynamic link to their submitted response.

You will:

- Create a **Utility** template named `form_response_template`.
- Add a **dynamic button URL** using `{{preview_code}}` to open the form response preview (e.g. `https://form.luluchat.io/preview/{{preview_code}}`).
- Map the template variables in **Luluchat Form Settings**.

---

## Step 1 – Create the template in WhatsApp Manager

You can open WhatsApp Manager in two ways:

- From Meta Business: Go to your **WhatsApp Manager** and open **Message Templates**.
- From Luluchat: In the **Inbox**, click **Create Template**. This will redirect you to WhatsApp Manager.

Once you are in the Message Templates page:

{% stepper %}
{% step %}
#### 1. Click **Create template**

1. In WhatsApp Manager, go to **Message templates**.
2. Click the **Create template** button.
{% endstep %}

{% step %}
#### 2. Select the **Utility** category

1. When asked to choose a template category, select the **Utility** tab.
2. Click **Next** to continue.
{% endstep %}

{% step %}
#### 3. Set template name and content

Fill in the basic template details:

1. **Template name**:
   Enter `form_response_template`.
2. **Language**:
   Choose the language you normally use for your customers (for example, English).
3. **Body**:
   Use the following body text (Meta will show variables as `{{1}}`, `{{2}}` later, but you can write the text first):

   ```text
   Hi {{submitter_name}}, we’ve successfully received your submission.

   You may check out your submitted response using the button below.
   ```

   - `{{submitter_name}}` will be a variable that Luluchat fills with the contact’s name later.
{% endstep %}

{% step %}
#### 4. Add a **Visit website** button with dynamic URL

1. Scroll to the **Buttons** section.
2. Click **Add button** and choose **Visit website**.
3. For **URL type**, select **Dynamic**.
4. In the **URL** field, enter:

   ```text
   https://form.luluchat.io/preview/{{preview_code}}
   ```

   - `{{preview_code}}` will be a variable that Luluchat fills with a unique preview code per response.

5. In **Add sample URL**, enter a sample URL for review, for example:

   ```text
   https://form.luluchat.io/preview/123456
   ```

   This sample value (e.g. `123456`) is only for Meta’s review, not used in production.
{% endstep %}

{% step %}
#### 5. Submit for review

1. Review your template name, category, body, and button configuration.
2. Click **Submit for review**.
3. Wait for Meta to review and approve the template.
   - While it is being reviewed, the template status will show as **In review**.
   - Once approved, the status will change to **Approved** and can be used in Luluchat.
{% endstep %}
{% endstepper %}

---

## Step 2 – Connect the template in Luluchat Form Settings

After you have created (or at least submitted) the template in WhatsApp Manager, you can link it to your form in Luluchat so that submitters receive the message and preview link.

1. In Luluchat, go to **Forms** and open the form you want to configure.
2. Go to the **Settings** tab for that form.
3. Find the option **“Select a message template to send response to recipients”**.

### 2.1 Select the WABA message template

1. Click **Select message template**.
2. In the template list, choose the `form_response_template` you created earlier.
   - You can select it even if the status is **In review**; once Meta approves it, it will start sending.

### 2.2 Map template variables

Luluchat will ask you to fill in the variables used in the template:

- **Body variable** – for `{{submitter_name}}`
- **Button variable** – for `{{preview_code}}`

Fill them as follows:

1. **Body variable**
   - Key in `{{submitter_name}}` (or select the submitter / contact name attribute offered by the UI).
   - This tells Luluchat to use the form submitter’s name for the greeting.

2. **Button variable**
   - Key in `{{preview_code}}`.
   - Luluchat will automatically replace `{{preview_code}}` with the unique code that points to the form response preview URL `https://form.luluchat.io/preview/{{preview_code}}`.

3. Click **Confirm** to save the variable mapping.

### 2.3 Save the form settings

1. After confirming the template and variables, click **Submit** (or **Save**) in the form settings page.
2. The form is now configured to:
   - Send the `form_response_template` via WhatsApp after a user submits the form.
   - Include a personalized greeting (using the submitter’s name).
   - Include a **button** that opens the form response preview page, for example:
     `https://form.luluchat.io/preview/123456`

---

## Important behavior to know

- **Template review time**: Meta may take a few minutes to several hours to approve the template. Until then, status will be **In review**.
- **Variable consistency**:
  - Make sure the variables you configure in Luluchat (e.g. `{{submitter_name}}`, `{{preview_code}}`) match the variables used in the template body and button URL.
- **Preview URL format**:
  - The final URL sent to users will follow the format:
    `https://form.luluchat.io/preview/{{preview_code}}`
  - Example: `https://form.luluchat.io/preview/123456`.

---

## Related documentation

- [Forms Overview](index.md)
- [Form Settings & SEO](settings.md)
- [Managing Responses](responses.md)
- [Message Templates](../message-templates.md)

