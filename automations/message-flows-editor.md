# Message Flow Editor

## Overview
The Message Flow Editor is a visual drag-and-drop builder where you design automated conversation paths. It allows you to map out exactly how Luluchat should respond to your customers based on their inputs and behavior.

---

## Editor Tools & Settings
On the right-hand side of the editor, you will find several tools to help you manage and organize your flow:

### 1. Flow Settings ⚙️
Manage the high-level behavior of your flow, specifically **Flow Trigger Limitation**.
- **Trigger Limits**: Prevent "spamming" by limiting how many times a flow can be triggered for the same user within a specific timeframe (e.g., maximum 1 time every 24 hours).
- **Default Flow Settings**: For system flows (like Away or Absent flows), you can set re-trigger conditions based on elapsed time since the last conversation.

### 2. Export as Image 📸
Download a high-resolution PNG image of your entire flow diagram. This is useful for sharing your automation logic with team members or keeping offline documentation.

### 3. Auto Layout 🏗️
Click this to automatically tidy up your workspace. Luluchat arranges all nodes from left to right, ensuring a clean and readable diagram. Nodes without links are placed neatly below the Starting Step.

---

## Adding Nodes (The "Add Node" Menu)
Click the **+ (Plus)** button on the right-hand side to add new steps to your flow. The menu is divided into three logical sections:

### 1. Starting & Complete Step
These nodes define the beginning and end of your automation.
- **Trigger**: The entry point of your flow. You can configure various triggers like Keywords, Growth Tools, or events.
- **Complete**: Marks the successful end of a flow path.

### 2. Content
These nodes are used to send information to the customer.
- **Message**: Send a standard WhatsApp text, image, or media message.
- **Message Template**: Send a pre-approved **WABA template** (required for initiating conversations or replying outside the 24-hour window).
- **Start Flow**: Redirect the customer to another existing Message Flow.
- **Form**: Send a link to a **Luluchat Form** to collect structured data.
- **AI Agent**: Connect your flow to **Praxus AI** for intelligent, dynamic responses (requires integration).

### 3. Logics
These nodes control the direction and behavior of the flow without necessarily sending a message.
- **Actions**: Perform background tasks like **Add Tag**, **Assign Assignee**, or **Update Custom Attribute**.
- **Round Robin**: Automatically distribute conversations or tasks among a group of team members in a circular order.
- **Smart Delay**: Pause the flow for a specific duration or until a specific time before moving to the next step.
- **Condition**: Create "If/Else" paths based on contact data (e.g., if the contact has a "VIP" tag, go to Path A; otherwise, go to Path B).
- **Randomizer**: Split your audience into different paths based on percentages (ideal for A/B testing different message variations).

📸 Screenshot placeholder:
> [Screenshot: Message Flow editor showing the right-hand toolbar and the Add Node menu expanded]

---

## Best practice 💡
- **Use Auto Layout**: Frequently use the Auto Layout tool to keep your flows manageable as they grow in complexity.
- **Set Trigger Limits**: Always configure trigger limits for marketing flows to ensure you don't overwhelm your customers with repeated messages.
- **Test with Randomizer**: Use the Randomizer node to test which message wording or offer gets better engagement from your audience.
