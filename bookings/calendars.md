# Calendars

## What is a Booking Calendar?

A Booking Calendar is a configurable scheduling system that allows customers to book appointments for your services. Each calendar has its own booking link, services, working hours, and settings. You can create multiple calendars for different purposes (e.g., different locations, service types, or staff members).

## When to use it?

* **New Service Offering**: Create a calendar when launching a new booking service.
* **Multiple Locations**: Set up separate calendars for different branches or locations.
* **Different Service Types**: Create dedicated calendars for different service categories.
* **Staff-Specific Booking**: Create calendars for individual staff members or teams.

## How to create a calendar (Step by Step)

{% stepper %}
{% step %}
#### Open Calendars Page

Go to `Bookings` > `Calendars` from the left menu.

📸 Screenshot placeholder:

> \[Screenshot: Calendars list page with "Create Calendar" button]
{% endstep %}

{% step %}
#### Click Create Calendar

Click the **"Create Calendar"** button at the top right of the page.

📸 Screenshot placeholder:

> \[Screenshot: Create Calendar button and modal/form opening]
{% endstep %}

{% step %}
#### Configure General Settings (Tab 1: General)

In the "General" tab, configure basic calendar information:

* **Cover Image**: Upload a cover image (recommended: 1065x390 pixels) that appears on the booking page.
* **Calendar Name**: Enter a name for your calendar (required, max 70 characters).
* **Calendar Link**: Set a unique URL slug for your booking link (e.g., "hair-salon" creates `booking.luluchat.io/your-team/hair-salon`).
* **Location**: Enter the physical location or address (optional).
* **Link Google Calendar**: Toggle to enable Google Calendar integration and generate Google Meet links.
  * If enabled, select a **Google Account** and **Google Calendar**.
  * **Note**: To use this feature, you must first connect your Google Calendar account in [Settings > Integration](settings/account/integration.md). See [Google Calendar Integration](settings/account/google-calendar-integration.md) for detailed setup instructions.
* **Description**: Add a description that appears on the booking page (max 255 characters).
* **Sort Order**: Set a number (0-1000) to control calendar display order (higher numbers appear first).
* **Working Hours**: Click to configure which days and hours appointments are available.
* **Is Publish**: Toggle to publish (make live) or unpublish the calendar.

📸 Screenshot placeholder:

> \[Screenshot: General tab with all fields filled, showing preview on the right side]

Click **Save** to save your general settings.
{% endstep %}

{% step %}
#### Add Services (Tab 2: Services)

In the "Services" tab, add the services customers can book:

1. Click **"Add Service"** button.
2. In the service form, configure:
   * **Service Name**: Name of the service (e.g., "Haircut", "Consultation").
   * **Service Description**: Description of what the service includes.
   * **Duration**: How long the service takes (in minutes).
   * **Sort Order**: Display order (0-1000, higher numbers first).
   * **Working Hours**: Select which working hours template applies to this service.
   * **Staff Assignment**: Choose how staff are assigned (All Staff, Specific Staff, or Round Robin).
   * **Minimum Notice**: How far in advance customers must book (None, 30 min, 1 hour, 2 hours, 3 hours, 4 hours).
3. Click **Save** to add the service.

📸 Screenshot placeholder:

> \[Screenshot: Services tab showing service list and Add Service form]

You can add multiple services to a single calendar. Customers will see all services when booking.
{% endstep %}

{% step %}
#### Configure Booking Form (Tab 3: Booking Form)

In the "Booking Form" tab, customize the information you collect from customers:

* **Default Fields**: First Name, Last Name, WhatsApp Contact No, and Email are required and cannot be removed, but you can rename them or change their order.
* **Add Questions**: Click the "+" button to add additional form fields:
  * Text, Phone, Date, Multiple Choice, Dropdown, Image, Video
* **Reorder Fields**: Drag and drop fields to change their order.
* **Required Fields**: Toggle which fields are required.

📸 Screenshot placeholder:

> \[Screenshot: Booking Form tab showing form builder with default and custom fields]

Click **Save** to save your form configuration.
{% endstep %}

{% step %}
#### Configure Settings (Tab 4: Settings)

In the "Settings" tab, configure booking behavior:

* **Disable No of Guests Selection**: Toggle to hide guest count selection (defaults to 1 guest if disabled).
* **Appointment Confirmation Mode**:
  * **Automatically Confirm Appointment**: Appointments are confirmed immediately.
  * **Manually Review and Confirm Appointment**: You must manually confirm each appointment.
* **Booking Window Limit**: Maximum days in advance customers can book (e.g., 30 days).
* **Limit bookings per time slot**: Toggle to restrict how many bookings can occur at the same time.
  * If enabled, set **Maximum bookings per time slot**.
* **Reminder Before Hour**: Set how many hours before the appointment to send a reminder (optional).

📸 Screenshot placeholder:

> \[Screenshot: Settings tab with all configuration options]

Click **Save** to save your settings.
{% endstep %}

{% step %}
#### Set Working Hours (Tab 5: Working Hours)

In the "Working Hours" tab, configure when appointments are available:

1. For each day of the week (Monday-Sunday):
   * Toggle the day **On** or **Off**.
   * If On, set **Start Time** and **End Time**.
   * Optionally add **Break Times** (periods when appointments are not available).
2. You can set different hours for different days.

📸 Screenshot placeholder:

> \[Screenshot: Working Hours tab showing day-by-day configuration with time selectors]

Click **Save** to save your working hours.
{% endstep %}

{% step %}
#### Set Off Dates (Tab 6: Off Dates)

In the "Off Dates" tab, mark dates when appointments are not available (holidays, closures):

1. Click **"Add Off Date"**.
2. Set **Start Date Time** and **End Date Time** for the closure period.
3. Click **Save** to add the off date.

📸 Screenshot placeholder:

> \[Screenshot: Off Dates tab showing list of off dates and Add Off Date form]
{% endstep %}

{% step %}
#### Configure Notifications (Tab 7: Notifications)

In the "Notifications" tab, set up automated messages:

1. **Tracked Events**: Select which events trigger notifications:
   * Appointment Created
   * Appointment Updated
   * Appointment Confirmed
   * Appointment Cancelled
   * Appointment Reminder
2. For each tracked event, configure:
   * **Message Subject**: Subject line for the notification.
   * **Message Template**: Message body with placeholders like `{{customer}}`, `{{reference_number}}`, `{{service_name}}`, `{{start_date_time}}`, etc.

📸 Screenshot placeholder:

> \[Screenshot: Notifications tab showing tracked events checkboxes and message template fields]

Click **Save** to save your notification settings.
{% endstep %}

{% step %}
#### Set Up Automation (Tab 8: Automation)

In the "Automation" tab, link Message Flows to booking events:

* **When Appointment is Done**: Select a Message Flow to trigger when an appointment is marked as "Done".
* **When Appointment is Cancelled**: Select a Message Flow to trigger when an appointment is cancelled.
* **When Appointment is No-Show**: Select a Message Flow to trigger when an appointment is marked as "No-Show".

📸 Screenshot placeholder:

> \[Screenshot: Automation tab showing flow selectors for done, cancelled, and no-show events]

Click **Save** to save your automation settings.
{% endstep %}

{% step %}
#### Publish and Share

Once your calendar is configured:

1. Ensure **"Is Publish"** is toggled **On** in the General tab.
2. Go back to `Bookings` > `Calendars` to see your calendar in the list.
3. Find your calendar and copy the booking link (displayed below the calendar name).
4. Share the link with customers via WhatsApp, email, or your website.

📸 Screenshot placeholder:

> \[Screenshot: Calendars list showing published calendar with QR code and booking link]
{% endstep %}
{% endstepper %}

## Managing Existing Calendars

### View Calendar List

Go to `Bookings` > `Calendars` to see all your calendars. Each calendar shows:

* Calendar name with booking link
* QR code (click "Download" to save)
* Sort order
* Actions: Preview, View Appointments, Duplicate, Delete

📸 Screenshot placeholder:

> \[Screenshot: Calendars list table with all columns and action buttons]

### Edit Calendar

1. Click the calendar name in the list to open the edit page.
2. Navigate through tabs to update any settings.
3. Click **Save** in each tab to save changes.

### Duplicate Calendar

Click the **Duplicate** icon (copy icon) to create a copy of an existing calendar with all its settings.

### Delete Calendar

Click the **Delete** icon (trash icon) and confirm to permanently delete a calendar.

### Preview Calendar

Click the **Preview** icon (eye icon) to see how the booking page appears to customers (only works if calendar is published).

## What happens after you create a calendar?

* **Booking Link Generated**: A unique URL is created that customers can use to book appointments.
* **QR Code Available**: A QR code is generated for easy sharing.
* **Appointments Can Be Booked**: Once published, customers can start booking appointments.
* **Notifications Sent**: If configured, automated notifications are sent for tracked events.
* **Automations Triggered**: Linked Message Flows run when corresponding events occur.

## Important behavior to know

* **Publishing Required**: Calendars must be published ("Is Publish" = Yes) before customers can access the booking link.
* **Unique Calendar Link**: Each calendar has a unique URL slug. If you change it, the old link will no longer work.
* **Working Hours Priority**: Service-specific working hours override calendar-wide working hours if configured.
* **Off Dates Override**: Off dates take precedence over working hours—no appointments can be booked on off dates.
* **Confirmation Mode**: If set to "Manual", appointments appear in the "Pending" tab until you confirm them.
* **Booking Window**: Customers cannot book beyond the "Booking Window Limit" you set.
* **Minimum Notice**: Customers cannot book appointments within the "Minimum Notice" period you set for each service.
* **Google Calendar Integration**: Requires Google Calendar integration to be set up in Settings > Integration first. When enabled, appointments are automatically created as events in your Google Calendar, and Google Meet links can be generated for virtual appointments. See [Google Calendar Integration](../settings/account/google-calendar-integration.md) for setup instructions.

## Common issues & solutions

* **Booking link not working**:
  * Ensure the calendar is published ("Is Publish" = Yes).
  * Check that the calendar link (unique\_code) doesn't contain invalid characters (use hyphens, not spaces).
* **No time slots available**:
  * Check that working hours are configured and the days are toggled "On".
  * Verify there are no off dates blocking the desired booking date.
  * Ensure services have working hours assigned.
* **Appointments not confirming automatically**:
  * Check "Appointment Confirmation Mode" in Settings—it may be set to "Manual".
* **Can't add Google Meet link**:
  * Ensure Google Calendar integration is connected in Settings > Integration. See [Google Calendar Integration](../settings/account/google-calendar-integration.md) for setup instructions.
  * Toggle "Link Google Calendar" to "Yes" in the General tab of your calendar.
  * Select a Google Account and Google Calendar from the dropdown menus.
* **Services not appearing**:
  * Make sure you've added services in the Services tab.
  * Verify services are saved and the calendar is published.

## Best practice 💡

* **Clear Service Names**: Use descriptive service names so customers understand what they're booking.
* **Set Realistic Durations**: Accurately set service durations to prevent double-booking.
* **Configure Working Hours**: Set working hours that match your actual availability to avoid conflicts.
* **Use Off Dates**: Mark holidays and closures in advance to prevent bookings on unavailable dates.
* **Enable Reminders**: Set up appointment reminders to reduce no-shows.
* **Test Booking Flow**: Before sharing, test the booking link yourself to ensure everything works correctly.
* **Monitor Appointments**: Regularly check the Appointments page to manage bookings and confirmations.

## Related Documentation

* [Appointments](appointments.md) - Learn how to view and manage customer appointments
* [Message Flows](../automations/message-flows.md) - Learn how to create automations for booking events
* [Google Calendar Integration](../settings/account/google-calendar-integration.md) - Learn how to connect Google Calendar to automatically create events for appointments