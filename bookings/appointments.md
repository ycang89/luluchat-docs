# Appointments

## What is Appointments?

Appointments is where you view and manage all customer bookings across your calendars. You can see appointments in list format (organized by status) or calendar format (visual timeline), and perform actions like confirming, rescheduling, cancelling, or marking appointments as done or no-show.

## When to use it?

* **Daily Management**: Check and manage appointments scheduled for today or upcoming days.
* **Confirm Bookings**: Review and confirm pending appointments (if using manual confirmation mode).
* **Reschedule**: Change appointment dates or times when customers request changes.
* **Track Status**: Monitor which appointments are confirmed, done, cancelled, or no-show.
* **Calendar View**: Get a visual overview of appointments across days or weeks.

## How to view appointments (Step by Step)

{% stepper %}
{% step %}
#### Open Appointments Page

Go to `Bookings` > `Appointments` from the left menu.

📸 Screenshot placeholder:

> \[Screenshot: Appointments page with tabs for Upcoming, Pending, Past]
{% endstep %}

{% step %}
#### Select View Type

Choose how you want to view appointments:

* List View: See appointments in a table format (default). Use the tabs:
  * Upcoming: Appointments scheduled for future dates.
  * Pending: Appointments waiting for manual confirmation (if confirmation mode is "Manual").
  * Past: Completed or past appointments.
* Calendar View: Click the "Calendar" button in the top right to switch to a visual calendar timeline.

📸 Screenshot placeholder:

> \[Screenshot: Appointments page showing tabs and Calendar button]
{% endstep %}

{% step %}
#### Filter Appointments (List View)

In list view, use the search filters to find specific appointments:

* Appointment Datetime: Select a date range to filter by booking date.
* Ref No.: Search by reference number.
* Name: Search by customer name.
* Calendar: Filter by specific calendar.
* Staff: Filter by staff member (if using staff assignment).

📸 Screenshot placeholder:

> \[Screenshot: List view with search filters expanded]
{% endstep %}

{% step %}
#### View Calendar View (Optional)

To see appointments in calendar format:

1. Click the "Calendar" button.
2. Select a Calendar from the dropdown (required).
3. Optionally select a Staff member to filter.
4. Use the view controls to switch between:
   * Day: See appointments for a single day.
   * Week: See appointments for the current week.
   * Agenda: See a list of upcoming appointments.

📸 Screenshot placeholder:

> \[Screenshot: Calendar view showing week view with appointments as colored blocks]
{% endstep %}
{% endstepper %}

In calendar view, appointments appear as colored blocks:

* **Green**: Confirmed appointments
* **Yellow**: Pending appointments
* **Red**: Cancelled appointments

## How to manage an appointment (Step by Step)

### Step 1: Open Appointment Details

Click on an appointment in either list or calendar view to open the appointment details modal.

📸 Screenshot placeholder:

> \[Screenshot: Appointment details modal showing all appointment information]

### Step 2: Review Appointment Information

The appointment details show:

* **Customer Information**: Name, contact number, email
* **Appointment Details**: Date, time, service, number of guests
* **Reference Number**: Unique booking reference
* **Status**: Current status (Pending, Confirmed, Done, Cancelled)
* **Calendar**: Which calendar the appointment belongs to
* **Staff**: Assigned staff member (if applicable)
* **Remarks**: Any notes or special requests

📸 Screenshot placeholder:

> \[Screenshot: Appointment form with all fields visible]

### Step 3: Edit Appointment (Optional)

To modify an appointment:

1. In the appointment details modal, update any editable fields:
   * **Service Slot**: Change to a different time slot (if available).
   * **Staff**: Reassign to a different staff member.
   * **Remarks**: Add or update notes.
2. Click **"Update Appointment"** to save changes.

📸 Screenshot placeholder:

> \[Screenshot: Appointment form with editable fields and Update button]

### Step 4: Change Appointment Status

Use the action buttons to change appointment status:

* **Confirm Appointment**: Click to confirm a pending appointment (only appears for pending appointments).
* **Mark as Done**: Click when the appointment is completed.
* **Cancel Appointment**: Click to cancel the appointment.
* **Mark as No-Show**: Click if the customer didn't attend the appointment.

📸 Screenshot placeholder:

> \[Screenshot: Action buttons for Confirm, Done, Cancel, No-Show]

Each action will ask for confirmation before proceeding.

## What happens after you manage appointments?

* **Status Updated**: The appointment status changes and appears in the appropriate tab.
* **Notifications Sent**: If configured, automated notifications are sent to customers (e.g., confirmation, cancellation).
* **Automations Triggered**: If Message Flows are linked to booking events (Done, Cancelled, No-Show), they will trigger.
* **Calendar View Updated**: The calendar view reflects status changes with updated colors.
* **List Refreshed**: The appointment list updates to show the new status.

## Important behavior to know

* **Pending Tab**: Only appears if your calendar's "Appointment Confirmation Mode" is set to "Manual". Otherwise, appointments are automatically confirmed.
* **Status Colors**:
  * Green = Confirmed or Done
  * Yellow = Pending
  * Red = Cancelled or No-Show
* **Rescheduling**: You can change the service slot, but only to available time slots. The system prevents double-booking.
* **No-Show Tag**: Appointments marked as "No-Show" display a red "No-Show" tag in the list view.
* **Reference Number**: Each appointment has a unique reference number that customers receive in confirmation messages.
* **Past Appointments**: Once an appointment date passes, it automatically moves to the "Past" tab.
* **Calendar Filter**: In calendar view, you must select a calendar to see appointments. You can filter by staff member as well.

## Common issues & solutions

* **Can't see appointments**:
  * Check that you've selected the correct calendar in calendar view.
  * Verify you're on the correct tab (Upcoming, Pending, or Past).
  * Ensure the calendar has appointments booked.
* **Pending tab is empty**:
  * If using automatic confirmation, appointments are confirmed immediately and won't appear in Pending.
  * Check that your calendar's confirmation mode is set to "Manual" if you want to review appointments.
* **Can't reschedule to desired time**:
  * The time slot may already be booked by another appointment.
  * Check that the desired time falls within working hours.
  * Verify there are no off dates blocking that date.
* **Calendar view shows no appointments**:
  * Ensure you've selected a calendar from the dropdown.
  * Check that the selected calendar has confirmed appointments in the date range you're viewing.
  * Try selecting a different staff member or clearing the staff filter.

## Best practice 💡

* **Regular Reviews**: Check the Pending tab daily if using manual confirmation to avoid delays.
* **Use Calendar View**: Use calendar view for a quick visual overview of your schedule, especially for busy days.
* **Mark No-Shows Promptly**: Mark no-shows as soon as possible to keep your records accurate.
* **Add Remarks**: Use the remarks field to note special requests or important customer information.
* **Confirm Quickly**: If using manual confirmation, confirm appointments promptly to provide good customer service.
* **Monitor Status**: Regularly review appointment statuses to ensure accurate tracking.

## Related Documentation

* [Calendars](calendars.md) - Learn how to create and configure booking calendars
* [Message Flows](../automations/message-flows.md) - Learn how to set up automations for appointment events
