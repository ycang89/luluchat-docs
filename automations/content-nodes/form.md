# Content: Form

## What is the Form Node?
The Form node sends an interactive web form link to the customer. This is the most efficient way to collect structured data (like emails, addresses, or file uploads) directly from WhatsApp.

## When to use it?
- **Lead Qualification**: Collect detailed requirements from a new prospect.
- **Support Requests**: Allow customers to upload images or documents for troubleshooting.
- **Surveys**: Get customer feedback after a purchase or service.

## How to set it up (Step by Step)
1. In the Message Flow Editor, click **Add Node (+) > Content > Form**.
2. Click the node to select one of your published **Luluchat Forms**.
3. Choose the channel you want to use for the automated delivery of the form.
4. You can also customize the message that accompanies the form link.

📸 Screenshot placeholder:
> [Screenshot: Form node configuration with a selected lead form and custom message]

## Important behavior to know
- **Automatic Identity**: Customers entering a form via this node are automatically identified by their WhatsApp number. They do not need to perform OTP verification.
- **Data Sync**: Answers collected in the form are automatically synced back to the contact's **Custom Attributes** in Luluchat.

## Best practice 💡
- **Complementary**: Use a Message node to explain *why* you are sending the form before the Form node appears.
- **Track Responses**: Regularly check the [Forms Module](../../forms/index.md) to see the data you've collected.
