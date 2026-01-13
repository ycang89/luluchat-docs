# Settings: Custom Attributes

## What is Custom Attributes?
Define personalized data fields to store contact information that matters to your business (e.g., "Last Purchase Date", "Preferred Language", "Account Manager").

## How to set it up (Step by Step)

### Step 1: Open Custom Attributes
Go to `Settings` > `Data Management` > `Custom Attributes`.

📸 Screenshot placeholder:
> [Screenshot: Custom Attributes list view]

### Step 2: Create an Attribute
Click `Create Custom Attribute`.
- **Name**: Choose a label that matches your terminology.
- **Data Type**: Select the type of information (e.g., Text, Number, Date) to ensure data consistency.

📸 Screenshot placeholder:
> [Screenshot: Create Custom Attribute form]

### Step 3: Organize and Export
- **Export**: Use the `Export Contacts` button to download a spreadsheet of your attributes.
- **Bulk Actions**: Select multiple attributes to delete them in one go.

📸 Screenshot placeholder:
> [Screenshot: Attribute list with selection checkboxes and footer toolbar]

> [!NOTE]
> **Important behavior to know**
>
> - **Variable Reuse**: Once defined, custom attributes can be inserted into Message Flows using variables (e.g., `{{Last_Purchase}}`) for personalized automation.
> - **Searchable**: You can filter your contact directory using these custom fields to create targeted lists.
> - **Bulk Deletion**: When deleting multiple custom attributes at once, ensure you're not removing attributes that are actively used in your Message Flows or contact profiles.

## Best practice 💡
- **Clean Terminology**: Avoid duplicate attributes by checking the list before creating new ones.
- **Integration Mapping**: Match attribute names to your external CRM or Shopify fields for seamless data syncing.
