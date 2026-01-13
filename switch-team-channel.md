# Switch Team and Channel

## What is Team and Channel Switching?

Team and Channel switching allows you to move between different teams and WhatsApp channels (phone numbers) from the header bar. This is useful when you're part of multiple teams or manage multiple WhatsApp business numbers.

## When to use it?

* **Multiple Teams**: If you're a member of multiple teams, switch between them to access different workspaces.
* **Multiple Channels**: If your team has multiple WhatsApp channels (phone numbers), switch between them to manage different business profiles or locations.
* **Different Workspaces**: Access different team settings, contacts, and conversations by switching teams.
* **Business Separation**: Manage separate WhatsApp numbers for different business units or brands.

## How to switch teams (Step by Step)

{% stepper %}
{% step %}
#### Locate Your Avatar

In the top right corner of the header bar, you'll see your name and avatar icon.

<figure><img src=".gitbook/assets/Screenshot 2026-01-13 at 5.41.18 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Click Your Avatar

Click on your name or avatar icon to open the dropdown menu.&#x20;
{% endstep %}

{% step %}
#### View Available Teams

In the dropdown menu, you'll see a "Switch Teams" section (or "Current Team" if you only have one team) listing all teams you're a member of. The current team will have a radio button selected.&#x20;
{% endstep %}

{% step %}
#### Select a Different Team

Click the radio button next to the team name you want to switch to. A "Switching Team..." message will appear, and the page will reload automatically.&#x20;
{% endstep %}

{% step %}
#### Wait for Page Reload

The page will automatically reload after switching teams. Once reloaded, you'll be in the selected team's workspace.&#x20;
{% endstep %}
{% endstepper %}

## How to switch channels (Step by Step)

{% stepper %}
{% step %}
#### Locate the Channels Button

In the header bar, look for the "Channels" button. It shows your current channel's phone number in parentheses (e.g., "Channels (+60123456789)").

<figure><img src=".gitbook/assets/Screenshot 2026-01-13 at 5.45.42 PM.png" alt=""><figcaption></figcaption></figure>

**Note**: If your channel is not connected, you'll see an exclamation mark icon and "Channel not connected" tooltip.
{% endstep %}

{% step %}
#### Click the Channels Button

Click the "Channels" button to open the Channels modal.
{% endstep %}

{% step %}
#### View Available Channels

The modal displays all channels (WhatsApp phone numbers) available in your current team. Each channel shows:

* Channel Name/Phone Number: The display name or phone number
* Status: Whether the channel is connected (ready) or needs setup
* Switch Button: Button to switch to that channel (or "Current Selected" if it's already active)

<figure><img src=".gitbook/assets/Screenshot 2026-01-13 at 5.41.47 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Switch to a Channel

Click the "Switch" button next to the channel you want to use. A "Redirecting to another Channel..." message will appear, and you'll be redirected to the Dashboard or Inbox.&#x20;
{% endstep %}

{% step %}
#### Verify Channel Switch

After switching, you'll see the new channel's phone number displayed in the Channels button in the header bar.

<figure><img src=".gitbook/assets/Screenshot 2026-01-13 at 5.48.12 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

## What happens after you switch?

* **Team Switch**:
  * All data (contacts, conversations, settings) changes to the selected team's data.
  * The page reloads to ensure all data is refreshed.
  * You'll see the team's name and channels in the header.
* **Channel Switch**:
  * You're redirected to Dashboard or Inbox (depending on channel status).
  * The header shows the new channel's phone number.
  * All conversations and contacts are filtered to the selected channel.
  * If switching to an unconnected channel, you'll see the channel setup page.

{% hint style="info" %}
**Important behavior to know**

* **Team Switch Reload**: Switching teams always reloads the page to ensure all data is refreshed for the new team.
* **Channel Status**: You can switch to channels even if they're not connected, but you'll need to complete the connection setup before using them.
* **Current Selection**: The current team and channel are always indicated with a selected radio button or "Current Selected" label.
* **Data Isolation**: Each team has its own contacts, conversations, settings, and channels. Data does not carry over between teams.
* **Single Team**: If you only belong to one team, the dropdown will show "Current Team" instead of "Switch Teams".
* **Channel Connection Required**: To use a channel for messaging, it must be connected (status: "ready"). Unconnected channels will show "Connect Now" instead of "Switch".
{% endhint %}

## How to Add a New Channel

If you need to connect multiple WhatsApp accounts or want to add another channel to your workspace, you can create additional channels:

{% stepper %}
{% step %}
**Access Channel Management**

1. Go to `Inbox` in the left menu.
2. If you have an existing channel connected, look for the channel selector or channel management option in the header or sidebar.
3. Alternatively, you can access channel management from the channel connection page.

📸 Screenshot placeholder:

> \[Screenshot: Inbox page showing channel selector or channel management option]
{% endstep %}

{% step %}
**Click Add Channel**

1. On the channel management page, you'll see a list of all your existing channels.
2. Click the **"Add Channel"** button at the bottom of the channel list.

📸 Screenshot placeholder:

> \[Screenshot: Channel list page showing "Add Channel" button]
{% endstep %}

{% step %}
**Connect Your New Channel**

1. After clicking "Add Channel", a new channel will be created.
2. You'll see a success message: "New Channel created, please scan and connect to your WhatsApp now."
3. The new channel will appear in your channel list with a "Not Connected" status.
4. Click **"Connect Now"** or select the new channel to start the connection process.
5. Follow the same connection steps as described in the sections above (either WhatsApp Personal or WhatsApp Cloud).

📸 Screenshot placeholder:

> \[Screenshot: New channel created showing "Connect Now" button]
{% endstep %}
{% endstepper %}

### Channel Limits

{% hint style="info" %}
**Channel Limits**: The number of channels you can create depends on your subscription plan. If you've reached your channel limit, you'll see a message indicating you need to upgrade. Click **"Need More Channel?"** to view upgrade options.
{% endhint %}

### Managing Multiple Channels

Once you have multiple channels:

* **Switch Between Channels**: Use the channel selector to switch between different channels. Each channel operates independently with its own contacts and conversations.
* **Current Selected Channel**: The channel you're currently using is marked as "Current Selected" in the channel list.
* **Channel Status**: Each channel shows its connection status (Connected/Not Connected) so you can easily see which channels are active.

## Common issues & solutions

* **Can't see other teams**:
  * You may only be a member of one team. Contact your team admin to be added to additional teams.
  * Check that you have the correct permissions to access multiple teams.
* **Team switch not working**:
  * Wait for the page reload to complete. Team switching requires a full page refresh.
  * If it still doesn't work, try refreshing the page manually or logging out and back in.
* **Channel not appearing**:
  * Ensure you're in the correct team (channels are team-specific).
  * Check that the channel exists and you have permission to access it.
  * Try refreshing the page.
* **Can't switch to unconnected channel**:
  * You can switch to unconnected channels, but you'll need to complete the connection setup first.
  * Click "Connect Now" or go to Inbox to set up the channel connection.
* **Wrong channel showing**:
  * Verify you've successfully switched by checking the phone number in the Channels button.
  * If the wrong channel is still showing, try switching again or refreshing the page.

## Best practice 💡

* **Use Clear Channel Names**: Give your channels descriptive names (e.g., "Main Business", "Support Line") to easily identify them when switching.
* **Verify After Switching**: Always check the header bar to confirm you're in the correct team and channel.
* **Team Organization**: Use separate teams for completely different businesses or organizations to keep data isolated.
* **Channel Organization**: Use multiple channels within the same team for different departments, locations, or business units.
* **Before Switching**: Save any unsaved work before switching teams, as the page will reload.

## Related Documentation

* [Connect your Channel](inbox/connect-channel.md) - Learn how to set up a new WhatsApp channel
* [Settings](settings/index.md) - Configure team and channel settings
