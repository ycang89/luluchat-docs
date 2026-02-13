# Google Calendar Integration

## What is Google Calendar Integration?

Google Calendar Integration allows you to connect your Google Calendar account with Luluchat. When enabled, appointments created through your Booking Calendars are automatically synced to your Google Calendar as events. You can also generate Google Meet links for virtual appointments.

## When does it trigger?

* When you want to automatically create calendar events for appointments booked through Luluchat.
* When you want to generate Google Meet links for virtual appointments.
* When you want to keep your Google Calendar in sync with your Luluchat bookings.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Access Integration Settings

Go to `Settings` from the left menu, then select `Account Management` > `Integration`.

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-13 at 3.20.28 PM.png" alt=""><figcaption></figcaption></figure>

> \[Screenshot: Settings page with Integration tab selected]
{% endstep %}

{% step %}
#### Find Google Calendar

Look for the **Google Calendar** card in the Apps grid. Click on it to open the Google Calendar integration page.
{% endstep %}

{% step %}
#### Connect Your Google Account

On the Google Calendar integration page, click the **"Connect"** or **"Connect Now"** button. This will redirect you to Google's OAuth page.
{% endstep %}

{% step %}
#### Authorize Luluchat

1. You'll be redirected to Google's sign-in page.
2. Sign in with the Google account that has access to the calendar you want to use.
3. Review the permissions that Luluchat is requesting (calendar access).
4. Click **"Allow"** or **"Continue"** to authorize the connection.

{% hint style="info" %}
**Permissions Required**: Luluchat needs access to view and manage your Google Calendar events to create appointments and generate meeting links.
{% endhint %}
{% endstep %}

{% step %}
#### Verify Connection

After authorizing, you'll be redirected back to Luluchat. You should see a success message confirming that your Google Calendar account is connected. The connected account will appear in the "Account Connected" section.
{% endstep %}
{% endstepper %}

## What happens after it triggers?

* **Account Connected**: Your Google Calendar account is now linked to Luluchat.
* **Available in Bookings**: You can now select this Google account and calendar when creating or editing booking calendars.
* **Automatic Event Creation**: When appointments are confirmed in your booking calendars, events are automatically created in your selected Google Calendar.
* **Google Meet Links**: If enabled, Google Meet links are automatically generated for virtual appointments.

## Using Google Calendar in Bookings

Once your Google Calendar is connected, you can use it in your booking calendars:

{% stepper %}
{% step %}
#### Enable Google Calendar in Your Calendar

1. Go to `Bookings` > `Calendars`.
2. Create a new calendar or edit an existing one.
3. In the **General** tab, toggle **"Link Google Calendar"** to **"Yes"**.

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-13 at 3.22.06 PM.png" alt=""><figcaption></figcaption></figure>

> \[Screenshot: Calendar General tab showing Link Google Calendar toggle]
{% endstep %}

{% step %}
#### Select Google Account and Calendar

1. After enabling "Link Google Calendar", you'll see dropdown menus for:
   * **Google Account**: Select the connected Google account you want to use.
   * **Google Calendar**: Select the specific calendar within that account where events should be created.
2. Optionally, include google\_meet\_link in template for recipient.

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-13 at 3.24.21 PM.png" alt=""><figcaption></figcaption></figure>

> \[Screenshot: Calendar General tab showing Google Account and Calendar dropdowns]
{% endstep %}

{% step %}
#### Save and Test

1. Click **Save** to save your calendar settings.
2. When a customer books an appointment and it's confirmed, an event will automatically be created in your selected Google Calendar.
3. If Google Meet is enabled, a meeting link will be generated and included in the event.
{% endstep %}
{% endstepper %}

## Managing Connected Accounts

### View Connected Accounts

1. Go to `Settings` > `Account Management` > `Integration`.
2. Click on the **Google Calendar** card.
3. In the "Account Connected" section, you'll see all connected Google accounts with their email addresses.

### Disconnect an Account

1. Go to `Settings` > `Account Management` > `Integration`.
2. Click on the **Google Calendar** card.
3. Find the account you want to disconnect in the "Account Connected" section.
4. Click the **"Disconnect"** button on that account's card.
5. Confirm the disconnection.

{% hint style="warning" %}
**Important**: Disconnecting a Google account will stop automatic event creation for any booking calendars using that account. You'll need to update those calendars to use a different Google account or disable Google Calendar integration.
{% endhint %}

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-13 at 3.27.01 PM.png" alt=""><figcaption></figcaption></figure>

> \[Screenshot: Disconnect button on Google account card]

## Important behavior to know

* **Multiple Accounts**: You can connect multiple Google accounts if needed. Each booking calendar can use a different Google account.
* **Calendar Selection**: You can choose which specific calendar within a Google account to use for each booking calendar.
* **Automatic Event Creation**: Events are only created when appointments are **confirmed**. Pending appointments won't create calendar events until they're confirmed.
* **Event Updates**: If an appointment is rescheduled or updated, the corresponding Google Calendar event is automatically updated.
* **Event Deletion**: If an appointment is cancelled, the corresponding Google Calendar event is automatically deleted from your calendar.
* **Google Meet Links**: Google Meet links are only generated if you enable "Generate Google Meet Link" in your booking calendar settings.
* **Event Details**: The calendar event includes appointment details like customer name, service name, duration, and reference number.
* **Attendees**: The customer's email (if provided) is automatically added as an attendee to the Google Calendar event.

## Common issues & solutions

* **"Connect" button not working**:
  * Check your browser's pop-up blocker settings. The OAuth flow may open in a pop-up window.
  * Try using a different browser or clearing your browser cache.
  * Ensure you have a stable internet connection.
* **Authorization failed**:
  * Make sure you're signing in with a Google account that has calendar access.
  * Check that you clicked "Allow" on the Google permissions page.
  * Try disconnecting and reconnecting the account.
* **Account not appearing in booking calendar dropdown**:
  * Ensure the account is successfully connected (check the Integration page).
  * Refresh the booking calendar page.
  * Try disconnecting and reconnecting the Google account.
* **Events not being created**:
  * Verify that "Link Google Calendar" is enabled in your booking calendar's General tab.
  * Ensure a Google Account and Calendar are selected.
  * Check that appointments are being confirmed (events are only created for confirmed appointments).
  * Verify the Google account still has proper permissions.
* **Google Meet link not generated**:
  * Ensure "Generate Google Meet Link" is enabled in your booking calendar settings.
  * Verify that your Google account has permission to create meeting links.
  * Check that the appointment has been confirmed.
* **Can't disconnect account**:
  * Make sure no active booking calendars are using that Google account. Update those calendars first, then disconnect.
  * Try refreshing the page and attempting to disconnect again.

## Best practice 💡

* **Use Dedicated Calendar**: Consider creating a separate Google Calendar specifically for Luluchat bookings to keep them organized.
* **Regular Sync Check**: Periodically check that events are being created correctly in your Google Calendar.
* **Test Before Going Live**: Test the integration with a test appointment before sharing your booking link with customers.
* **Monitor Permissions**: If you change Google account passwords or permissions, you may need to reconnect the account.
* **Backup Important Events**: While events are automatically synced, consider keeping a backup of important appointment information.
* **Use Google Meet for Virtual Appointments**: Enable Google Meet link generation for virtual consultations or remote services.

## Related Documentation

* [Integration Settings](integration.md) - Learn how to manage all integrations
* [Calendars](../bookings/calendars.md) - Learn how to create and configure booking calendars
* [Appointments](../bookings/appointments.md) - Learn how to manage appointments
* [Bookings Overview](../bookings/index.md) - Learn about the Bookings module
