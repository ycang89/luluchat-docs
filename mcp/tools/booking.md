# Booking

Tools for looking up [Bookings](../../bookings/index.md) calendars and appointments. These tools are read-only.

{% hint style="info" %}
**Typical flow:** `get_contact_booking_appointments` → `get_booking_appointment`
{% endhint %}

### get\_booking\_calendars

**Read** · List your booking calendars, optionally with working days, services and booking form.

**Example prompt:** *"Show me all booking calendars and their services."*

| Parameter | Required | Description |
| --- | --- | --- |
| `search` | No | Search by calendar name or description |
| `includes` | No | Comma-separated extras: `working_days`, `services`, `form` |
| `sort` | No | `name` (default), `created_at` or `sequence` |
| `order` | No | `asc` (default) or `desc` |
| `page` / `per_page` | No | Pagination (default 20 per page, max 100) |

### get\_contact\_booking\_appointments

**Read** · List a contact's appointments. By default only upcoming and ongoing appointments are returned.

**Example prompt:** *"Does +60123456789 have any confirmed appointments this month?"*

| Parameter | Required | Description |
| --- | --- | --- |
| `contact_number` | Yes | Contact number |
| `status` | No | `pending`, `confirmed`, `done` or `cancelled` |
| `date_range` | No | `{ "from": "YYYY-MM-DD", "to": "YYYY-MM-DD" }` (both required) |
| `include_past` | No | Include past appointments (default `false`) |
| `calendar_id` | No | Only appointments in this calendar |
| `page` / `per_page` | No | Pagination (default 20 per page, max 100) |

### get\_booking\_appointment

**Read** · Get the full details of one appointment by its ID or reference number.

**Example prompt:** *"Show me the details of appointment BK-2024-001 for +60123456789."*

| Parameter | Required | Description |
| --- | --- | --- |
| `contact_number` | Yes | Contact number (the appointment must belong to this contact) |
| `id_type` | Yes | `id` or `reference_number` |
| `booking_id` | Yes | The appointment ID or reference number, e.g. `BK-2024-001` |
| `includes` | No | Comma-separated extras: `customer`, `service`, `calendar`, `form_response` |
