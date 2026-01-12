# Content: AI Agent

## What is the AI Agent Node?
The AI Agent node connects your Message Flow to **Praxus AI**, allowing for dynamic, intelligent conversations that go beyond standard predefined paths.

## When to use it?
- **Intelligent FAQ**: Let the AI answer varied customer questions based on your knowledge base.
- **Natural Language Input**: Allow customers to type freely rather than just clicking buttons.
- **Dynamic Routing**: Use the AI to understand customer intent and route them to the correct path.

## How to set it up (Step by Step)
1. Ensure you have an active integration with **Praxus AI** in your [AI Settings](../../settings/tools/ai.md).
2. In the Message Flow Editor, click **Add Node (+) > Content > AI Agent**.
3. Click the node to configure the agent's behavior and the specific AI model or instructions it should follow.
4. Define the **Exit Points** for the AI agent (e.g., when the agent needs to hand over to a human or has completed its goal).

📸 Screenshot placeholder:
> [Screenshot: AI Agent node with configuration for intelligent handover]

## Important behavior to know
- **Requires Integration**: This node is only functional if you have a valid Praxus AI API key configured.
- **Token Usage**: Conversations handled by this node may consume AI tokens based on your Praxus AI plan.

## Best practice 💡
- **Hybrid Approach**: Use standard Message nodes for simple "Yes/No" questions and the AI Agent node for more open-ended discussions.
- **Monitor AI Handover**: Always define clear exit paths so customers aren't stuck talking to an AI if they need human assistance.
