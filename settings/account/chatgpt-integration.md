# ChatGPT Integration

## What is ChatGPT Integration?
ChatGPT Integration allows you to connect OpenAI's ChatGPT with Luluchat, enabling AI-powered features like intelligent message suggestions, content improvement, and automated responses in your Message Flows.

## When does it trigger?
- When you want to use AI-powered features in Luluchat, such as message suggestions or content improvement.
- When you need AI agents in your Message Flows to provide intelligent, context-aware responses.

## Prerequisites
- You must have an OpenAI account
- You will need to generate an API Key from your OpenAI account

## How to set it up (Step by Step)

### Part 1: Generate OpenAI API Key

{% stepper %}
{% step %}
### Sign Up or Log In to OpenAI

Sign up or log in to your OpenAI account at [https://platform.openai.com](https://platform.openai.com).

📸 Screenshot placeholder:
> [Screenshot: OpenAI platform login page]
{% endstep %}

{% step %}
### Create a New API Key

Go to [https://platform.openai.com/account/api-keys](https://platform.openai.com/account/api-keys) and click **Create new secret key** to get your API Key.

{% hint style="warning" %}
**Important**: Copy and save this API key immediately. You won't be able to see it again after closing the dialog.
{% endhint %}

<figure><img src="../../.gitbook/assets/Screenshot 2023-07-04 at 8.30.21 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

### Part 2: Connect ChatGPT in Luluchat

{% stepper %}
{% step %}
### Access the Apps Section

To access this module, in the side navigation menu, click **Apps**. Alternatively, go to `Settings` > `Account Management` > `Integration` and scroll to the Apps section.

📸 Screenshot placeholder:
> [Screenshot: Apps section in Integration settings]
{% endstep %}

{% step %}
### Click on ChatGPT App

Click on the **ChatGPT** app card to open the connection page.

<figure><img src="../../.gitbook/assets/Screenshot 2023-07-04 at 8.22.24 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Enter Your API Key

Enter the **API Key** you copied from OpenAI. Once you have filled in the required information, click on the **Save** button.

<figure><img src="../../.gitbook/assets/Screenshot 2023-07-04 at 8.23.11 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

## What happens after it triggers?
- **AI Features Enabled**: ChatGPT-powered features become available throughout Luluchat.
- **Message Suggestions**: You can use AI to get intelligent message suggestions and content improvements.
- **AI Agents Available**: You can add AI Agent nodes to your Message Flows for intelligent, context-aware conversations.

## Important behavior to know
- **API Key Security**: Your OpenAI API Key is sensitive information. Keep it secure and never share it publicly.
- **Usage Costs**: Using ChatGPT features may incur costs based on your OpenAI plan and usage. Monitor your OpenAI usage dashboard.
- **Key Storage**: The API key is stored securely in your browser. If you clear browser data, you may need to reconnect.
- **Model Access**: Ensure your OpenAI account has access to the models you want to use (e.g., GPT-4, GPT-3.5-turbo).

## Common issues & solutions
- **Connection failed**: Verify that you copied the entire API key correctly without any extra spaces. Ensure the key hasn't been revoked in OpenAI.
- **API errors**: Check your OpenAI account balance and usage limits. Ensure your API key has the necessary permissions.
- **Features not working**: Verify that the integration is active and that you've saved the API key successfully. Try disconnecting and reconnecting if issues persist.

## Best practice 💡
- **Secure Key Storage**: Store your OpenAI API key in a secure password manager.
- **Monitor Usage**: Regularly check your OpenAI usage dashboard to track costs and ensure you're within your budget.
- **Test Features**: After connecting, test AI features like message suggestions to ensure everything is working correctly.
- **Key Rotation**: Consider rotating your API keys periodically for enhanced security.

## Related Documentation
- [Integration Settings](./integration.md) - Learn how to manage your integrations
- [AI Agent Node](../automations/content-nodes/ai-agent.md) - Learn how to use AI agents in Message Flows
- [AI Settings](../tools/ai.md) - Learn about AI configuration options
