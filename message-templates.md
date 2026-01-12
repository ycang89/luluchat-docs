# Message Templates

## What is Message Templates?
Message Templates are pre-approved message formats used exclusively for **WhatsApp Cloud (WABA)** channels. They allow businesses to initiate conversations with customers or respond to them outside the 24-hour messaging window while staying compliant with WhatsApp's policies.

## When does it trigger?
- When you want to send a broadcast to customers.
- When you need to reply to a customer more than 24 hours after their last message.
- When setting up automated notifications in Message Flows.

## How to set it up (Step by Step)

### Step 1: Access Message Templates
Click `Message Templates` in the left menu. Here you will see a list of your existing templates and their current approval status.

📸 Screenshot placeholder:
> [Screenshot: Message Templates list showing template names, status, and languages]

### Step 2: Create a New Template
Click the **Create Message Template** button.

Luluchat will show a confirmation dialog explaining that you will be redirected to the **Meta WhatsApp Manager**. This is because all templates must be created and reviewed within Meta's official platform.

1. Click **Go to Meta WhatsApp Manager**.
2. Log in to your Meta Business account.
3. Follow Meta's instructions to define your template (Header, Body, Footer, and Buttons).
4. Submit the template for review.

📸 Screenshot placeholder:
> [Screenshot: Redirection confirmation dialog to Meta WhatsApp Manager]

### Step 3: Syncing Templates back to Luluchat
Once you have finished creating your template in the Meta WhatsApp Manager, return to Luluchat.

**CRITICAL STEP**: The new template will not appear in Luluchat automatically. You must manually sync them.
1. Click the **Sync from WhatsApp Manager** button located at the top right of the templates table.
2. Wait for the success message: "Synced successfully."
3. Your new template should now appear in the list with its latest status.

📸 Screenshot placeholder:
> [Screenshot: "Sync from WhatsApp Manager" button highlighted in the toolbar]

---

## Understanding Template Status
- **In review (Pending)**: WhatsApp is still reviewing your template. You cannot send it yet.
- **Active (Approved)**: The template is ready to use in Broadcasts or Flows. It will also show a Quality Score (e.g., High, Medium, Low).
- **Rejected**: WhatsApp has declined the template. Check the **Top block reason** column to understand why (e.g., promotional content, formatting errors).

## What happens after it triggers?
Once a template is approved and synced, it becomes available as a selection in:
- **Broadcasts**: To reach out to a large list of recipients.
- **Message Flows**: Within a "Send WhatsApp Message" action node.

## Important behavior to know
- **WABA Only**: Message Templates are only available for WhatsApp Cloud accounts. Standard WhatsApp Personal accounts do not use templates.
- **Approval Time**: WhatsApp review can take anywhere from a few minutes to 24 hours.
- **Variables**: If your template includes variables (e.g., `{{1}}`), you will need to map these to contact attributes (like Name or Order ID) inside Luluchat when using the template.

## Common issues & solutions
- **Template not showing**: Ensure you clicked the **Sync from WhatsApp Manager** button after creating it on Meta.
- **Rejected status**: Review Meta's guidelines. Common reasons include missing variables, unclear category selection, or using disallowed language.
- **Cannot delete**: Deleting a template in Luluchat only removes it from the local view. It is recommended to manage deletions directly in Meta WhatsApp Manager.

## Best practice 💡
- **Keep it Simple**: Use clear and concise language to speed up the approval process.
- **Test Variables**: Always double-check that your variable mapping is correct before sending a large broadcast.
- **Check Quality Score**: If your quality score drops to "Low", your template might get paused. Ensure your messages are relevant and not spammy.
