# Forms: Building a Form

## How to Build a Form (Step 1)
Go to `Forms` in the left menu and click a form to open it (or create a new one). The **1. Build Form** tab shows your form's questions in order.

Every new form starts with a title and two required questions, **Name** and **WhatsApp Contact No**. These two are compulsory: you can rename them or change their order, but not remove them.

<figure><img src="../.gitbook/assets/forms-build.png" alt="Build Form tab showing a Customer Feedback form"><figcaption><p>Build Form tab</p></figcaption></figure>

### Adding Questions
Click **Add Questions** at the bottom of the form and pick an element:

| Element | Use it for |
| --- | --- |
| **Title** | A heading and description for your form or a section |
| **Text** / **Textarea** | Short answers, or longer open-ended feedback |
| **Email** | Email addresses |
| **Phone** | Extra contact numbers (the country code is guessed automatically) |
| **Multiple Choice** | Pick one option. Options can have images. |
| **Checkbox** | Pick one or more options |
| **Dropdown** | Pick one option from a list |
| **Date** / **Time** | Booking requests or availability |
| **Image** / **Video** | Visual instructions or promotional content |
| **Files** | Let customers upload receipts, documents or photos |

{% hint style="warning" %}
**File Storage Required**: To use the Files element, you need the "File Storage 200G" add-on. Go to `Settings` > `Account Management` > `Billing` to view and purchase storage add-ons.
{% endhint %}

### Editing and ordering questions
- **Edit**: Click a question to open its settings panel.
- **Reorder**: Use the **Move Up** and **Move Down** arrows next to a question.
- **Remove**: Click the red **minus** icon next to a question.

### Question settings
When you click a question, you can set:

| Setting | Description |
| --- | --- |
| **Question text** | The question the customer sees |
| **Question details** | Extra instructions shown under the question |
| **Options** | The choices, for Multiple Choice, Checkbox and Dropdown |
| **Column Heading for Response** | A short name used as the column heading in [Responses](responses.md), e.g. `Rating` |
| **Custom Attribute to Save Response** | Save the answer to a contact's custom attribute |
| **Required** | The customer must answer before submitting |

### Mapping to Custom Attributes
Link a question to a **Custom Attribute** and the answer is saved to the contact's profile as soon as the form is submitted. For example, map *Which outlet did you visit?* to `favourite_outlet`, then use it to personalise your message flows.

<figure><img src="../.gitbook/assets/forms-question-settings.png" alt="Question settings panel with Custom Attribute to Save Response set to favourite_outlet" width="360"><figcaption><p>Question settings panel</p></figcaption></figure>

Click **Submit** at the bottom of the tab to save your changes. Use **Open Form Link** at the top right to preview the live form.

## Important behavior to know

* **Compulsory fields**: **Name** and **WhatsApp Contact No** are always part of the form. You can rename and reorder them, but not delete them.
* **File Upload Storage**: The Files element requires the "File Storage 200G" add-on. Without it, you can't add file upload questions. Go to `Settings` > `Account Management` > `Billing` to purchase it.
* **File Size Limits**: Uploaded files are subject to size limits based on your storage plan. Check your plan details for specific limits.

## Best practice 💡
- **Keep it Short**: Only ask for essential information to increase submission rates.
- **Use Clear Labels**: Make sure your questions are easy to understand.
- **Set Column Headings**: Give long questions a short column heading so the Responses table stays readable.
- **Required Fields**: Mark critical questions as **Required** so you get the data you need.
- **Plan Ahead for File Uploads**: If you need to collect documents or images, get the File Storage add-on before creating your form.
