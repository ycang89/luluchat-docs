# Custom Attributes

## What is Custom Attributes?

Define personalized data fields to store contact information that matters to your business (e.g., "Last Purchase Date", "Preferred Language", "Account Manager").

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Open Custom Attributes

Go to `Settings` > `Data Management` > `Custom Attributes`.

<figure><img src="../../.gitbook/assets/settings-custom-attributes.png" alt="Custom Attributes list"><figcaption><p>Custom Attributes (sample data)</p></figcaption></figure>
{% endstep %}

{% step %}
#### Create an Attribute

Click `Create Custom Attribute`.

* Name: Choose a label that matches your terminology.
* Data Type: **Text**, **Number**, **Date**, **Time** or **Anniversal Date** (a day and month that repeats every year, e.g. a birthday).

Click **Submit**.

<figure><img src="../../.gitbook/assets/settings-custom-attributes-create.png" alt="Create Custom Attribute dialog with name and data type" width="440"><figcaption><p>Create Custom Attribute</p></figcaption></figure>
{% endstep %}

{% step %}
#### Organize and Export

* Edit: Click an attribute's name to change it.
* Export: Click `Export Contacts` to download your list of custom attributes as an Excel file.
* Bulk Actions: Select multiple attributes to delete them in one go.

{% endstep %}
{% endstepper %}

{% hint style="info" %}
**Important behavior to know**

* **Variable Reuse**: Once defined, custom attributes can be inserted into Message Flows using variables (e.g., `{{Last_Purchase}}`) for personalized automation.
* **Searchable**: You can filter your contact directory using these custom fields to create targeted lists.
* **Bulk Deletion**: When deleting multiple custom attributes at once, ensure you're not removing attributes that are actively used in your Message Flows or contact profiles.
{% endhint %}

## Best practice 💡

* **Clean Terminology**: Avoid duplicate attributes by checking the list before creating new ones.
* **Integration Mapping**: Match attribute names to your external CRM or Shopify fields for seamless data syncing.
