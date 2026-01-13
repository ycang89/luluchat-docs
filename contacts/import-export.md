# Import & Export

## Growing Your Audience

Luluchat makes it easy to bring your existing audience into the platform or export your data for use in other tools.

### Importing Contacts

If you have a large list of customers, you can add them all at once:

{% stepper %}
{% step %}
#### Click Import Contacts

Click the **Import Contacts** button in the Contacts page.
{% endstep %}

{% step %}
#### Download Excel Template

Download the **Excel Template** provided by Luluchat to ensure your file format is correct.
{% endstep %}

{% step %}
#### Fill in Contact Details

Fill in your contact details in the template (Name, Phone Number, Tags, etc.).

**Updating Existing Contacts**: You can use the import to update existing contacts. If a contact with the same phone number already exists, the import will update their information with the new data from your Excel file.

**Tag Column Format**: In the Tags column, you can add multiple tags by separating them with commas. For example:
- `"old tag, new tag"` will add both "old tag" and "new tag" to the contact
- If a tag doesn't exist yet, it will be **automatically created** during the import
- Multiple tags should be separated by commas (e.g., `"VIP, Customer, Newsletter"`)

📸 Screenshot placeholder:
> [Screenshot: Excel template showing Tags column with comma-separated values]
{% endstep %}

{% step %}
#### Upload and Import

Upload the completed file and click **Import** to submit your import request. The import will be processed in the background.

{% hint style="info" %}
**Processing Time**: Once you submit the import request, the server will process it in the background. You're free to continue using Luluchat while the import runs. Processing usually takes **1 to 15 minutes**, depending on the number of contacts and server readiness. You'll receive a notification once the import is complete.
{% endhint %}
{% endstep %}
{% endstepper %}

### Exporting Audience Data

To download your contact list:

{% stepper %}
{% step %}
#### Apply Filters (Optional)

Apply any filters (e.g., filter by a specific tag) if you only want a subset of your audience.
{% endstep %}

{% step %}
#### Click Export

Click the **Export** button in the Contacts page.
{% endstep %}

{% step %}
#### Download Excel File

An Excel file containing all visible contacts and their details will be downloaded automatically.
{% endstep %}

{% endstepper %}

📸 Screenshot placeholder:

> \[Screenshot: Import Contacts modal with the template download link]

## Important behavior to know

* **Phone Number Format**: Always ensure phone numbers include the country code (e.g., 60123456789).
* **Duplicate Handling**: The system will automatically detect existing contacts based on their phone number and update their information rather than creating duplicates.
* **Updating Contacts**: You can update existing contacts by importing an Excel file with the same phone numbers. The import will update the contact's information (name, tags, custom attributes, etc.) with the new data from your file.
* **Multiple Tags**: In the Tags column, separate multiple tags with commas (e.g., `"old tag, new tag"`). The import will add all specified tags to the contact.
* **Auto-Create Tags**: If a tag in your import file doesn't exist yet, it will be automatically created during the import process. You don't need to create tags manually before importing.
* **Background Processing**: Import requests are processed in the background. You can continue using Luluchat while the import runs. Processing typically takes 1 to 15 minutes depending on the number of contacts and server readiness.
* **Notifications**: You'll receive a notification once your import is complete. Check your notifications to see when the import has finished.