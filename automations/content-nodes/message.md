# Content: Message

## What is the Message Node?
The Message node is the standard way to send text and media to your customers during an active 24-hour conversation window.

## Supported Content
You can add multiple blocks of content within a single Message node:
- **Text**: Standard text messages with support for emojis and markdown (bold, italic).
- **Image**: Send JPG or PNG files.
- **Video**: Send MP4 files.
- **Audio**: Send voice notes or recordings.
- **File**: Send PDFs or other documents.
- **Interactive Buttons**: Add buttons that customers can click to reply quickly or trigger the next step.

## How to set it up (Step by Step)
1. In the Message Flow Editor, click **Add Node (+) > Content > Message**.
2. Click the node to open the content builder.
3. Click **Add Content** to choose the type of block you want to add.
4. Type your message or upload your media.
5. If using buttons, click **Add Button** and define the label. You can then link each button to a different path in your flow.

📸 Screenshot placeholder:
> [Screenshot: Message node builder with a text block and two buttons configured]

## Important behavior to know
- **24-Hour Window**: This node only works if the customer has messaged you within the last 24 hours. Outside of this window, you must use a **Message Template**.
- **Sequential Sending**: If you add multiple content blocks (e.g., an Image followed by Text), they will be sent to the customer in that order.

## Best practice 💡
- **Use Media**: Messages with images or videos often get higher engagement than plain text.
- **Quick Replies**: Use buttons instead of asking customers to type their answers to reduce friction.
- **Personalize**: Use placeholders (e.g., `{{name}}`) to make the message feel more personal.
