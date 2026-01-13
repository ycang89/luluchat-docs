# Contacts: Bulk Updates & Advanced Actions

## What is Bulk Updates & Advanced Actions?
Bulk Updates and Advanced Actions allow you to manage multiple contacts at once, saving time when working with large contact lists. Instead of updating contacts one by one, you can select multiple contacts and apply changes to all of them simultaneously.

## When to use it?
- **Segmenting Contacts**: Add or remove tags from multiple contacts to organize them into categories.
- **Reassigning Workload**: Transfer contacts from one team member to another when responsibilities change.
- **Mass Updates**: Update contact properties, opt-in status, or list memberships for many contacts at once.
- **Team Restructuring**: Reassign contacts when team members leave or roles change.

## Bulk Add Tags (Step by Step)

{% stepper %}
{% step %}
### Select Contacts

In the Contacts list, use the checkboxes on the left to select the contacts you want to add tags to. You can select individual contacts or use the checkbox in the table header to select all contacts on the current page.

📸 Screenshot placeholder:
> [Screenshot: Contacts list with multiple contacts selected using checkboxes]
{% endstep %}

{% step %}
### Open Bulk Update

After selecting contacts, a toolbar appears at the bottom of the page. Click the Bulk Update button.

📸 Screenshot placeholder:
> [Screenshot: Bottom toolbar showing Bulk Update button with selected contacts count]
{% endstep %}

{% step %}
### Choose Add Tags Action

In the "Bulk Update Contacts" modal, select Add Tags from the "Action" dropdown.

📸 Screenshot placeholder:
> [Screenshot: Bulk Update modal with Action dropdown showing "Add Tags" option]
{% endstep %}

{% step %}
### Select Tags

In the "Tags" field, select one or more tags you want to add to the selected contacts. You can select multiple tags at once.

📸 Screenshot placeholder:
> [Screenshot: Tags dropdown with multiple tags selected]
{% endstep %}

{% step %}
### Submit

Click the submit button to apply the tags. You'll see a success message confirming that all selected contacts have been updated.

📸 Screenshot placeholder:
> [Screenshot: Success message confirming tags added]
{% endstep %}
{% endstepper %}

## Bulk Remove Tags (Step by Step)

{% stepper %}
{% step %}
### Select Contacts

In the Contacts list, use the checkboxes to select the contacts you want to remove tags from.

📸 Screenshot placeholder:
> [Screenshot: Contacts list with contacts selected]
{% endstep %}

{% step %}
### Open Bulk Update

Click the Bulk Update button in the bottom toolbar.

📸 Screenshot placeholder:
> [Screenshot: Bulk Update button in toolbar]
{% endstep %}

{% step %}
### Choose Remove Tags Action

In the "Bulk Update Contacts" modal, select Remove Tags from the "Action" dropdown.

📸 Screenshot placeholder:
> [Screenshot: Bulk Update modal with "Remove Tags" selected in Action dropdown]
{% endstep %}

{% step %}
### Select Tags to Remove

In the "Tags" field, select the tags you want to remove from the selected contacts. You can select multiple tags to remove them all at once.

📸 Screenshot placeholder:
> [Screenshot: Tags dropdown showing tags to remove]
{% endstep %}

{% step %}
### Submit

Click the submit button to remove the tags. You'll see a success message confirming that all selected contacts have been updated.

📸 Screenshot placeholder:
> [Screenshot: Success message confirming tags removed]
{% endstep %}
{% endstepper %}

## Bulk Transfer Assignee (Step by Step)

{% stepper %}
{% step %}
### Open Advanced Actions

In the Contacts list, click the Advanced Actions button in the top toolbar (not the Bulk Update button).

📸 Screenshot placeholder:
> [Screenshot: Contacts list showing Advanced Actions button in toolbar]
{% endstep %}

{% step %}
### Choose Transfer Assignee Action

In the "Advanced Actions" modal, select Transfer Assignee from the "Action" dropdown.

📸 Screenshot placeholder:
> [Screenshot: Advanced Actions modal with "Transfer Assignee" selected]
{% endstep %}

{% step %}
### Select Source Assignee

In the "From Assignee A" field, select the team member whose contacts you want to transfer. This will transfer ALL contacts assigned to this person, not just selected ones.

📸 Screenshot placeholder:
> [Screenshot: From Assignee A dropdown with team member selected]
{% endstep %}

{% step %}
### Select Destination Assignee

In the "To Assignee B" field, select the team member who should receive the contacts.

📸 Screenshot placeholder:
> [Screenshot: To Assignee B dropdown with destination team member selected]
{% endstep %}

{% step %}
### Review Warning

Read the tip about disabling "Assignee Changes" workflows before proceeding, as they could trigger unintended automation reactions.

📸 Screenshot placeholder:
> [Screenshot: Warning message about disabling workflows]
{% endstep %}

{% step %}
### Submit

Click the submit button to transfer all contacts from Assignee A to Assignee B. You'll see a success message confirming the transfer. The message will indicate that you may need to refresh the list to see the changes.

📸 Screenshot placeholder:
> [Screenshot: Success message confirming assignee transfer]
{% endstep %}
{% endstepper %}

## What happens after bulk operations?

### Bulk Add/Remove Tags
- **Immediate Update**: Tags are immediately added or removed from all selected contacts.
- **No Data Loss**: Removing tags doesn't delete the contacts or other tags. Contacts retain all their other tags.
- **Multiple Tags**: You can add or remove multiple tags in a single operation.

### Bulk Transfer Assignee
- **Complete Transfer**: ALL contacts assigned to the source assignee are transferred to the destination assignee, not just contacts visible on the current page.
- **Automatic Update**: The transfer happens automatically across all contacts in your database.
- **Workflow Impact**: If you have "Assignee Changes" workflows enabled, they may trigger automatically. Consider disabling them before bulk transfers to avoid unintended automation reactions.
- **Refresh Required**: You may need to refresh the contacts list to see the updated assignments.

{% hint style="warning" %}
**Important behavior to know**

### Bulk Add/Remove Tags
- **Multiple Selection**: You can select multiple tags to add or remove in a single operation.
- **Existing Tags**: Adding a tag that a contact already has won't cause an error - the tag is simply maintained.
- **No Impact on Other Tags**: Removing specific tags doesn't affect other tags on the contacts.
- **Selection Required**: You must select at least one contact before the Bulk Update button becomes available.

### Bulk Transfer Assignee
- **All Contacts Transferred**: The transfer affects ALL contacts assigned to the source assignee, regardless of filters or current page view.
- **Workflow Considerations**: If you have workflows that trigger on assignee changes, they will fire for each transferred contact. This could cause a chain reaction of automations.
- **One-Way Transfer**: This is a complete transfer - contacts move from Assignee A to Assignee B. You cannot undo this action easily.
- **Deleted Team Members**: If a team member is deleted, their name will appear with a "[DELETED]" prefix in the dropdown, but you can still transfer their contacts.
{% endhint %}

## Common issues & solutions

- **Bulk Update button not appearing**:
  - Ensure you've selected at least one contact using the checkboxes.
  - The Bulk Update button appears in the bottom toolbar after selection.

- **Tags not updating**:
  - Verify that you selected the correct action (Add Tags vs Remove Tags).
  - Check that the tags you selected exist in your Tags settings.
  - Refresh the contacts list to see updated tags.

- **Transfer Assignee affecting wrong contacts**:
  - Remember that Transfer Assignee affects ALL contacts assigned to the source assignee, not just selected ones.
  - Review the source assignee's contact count before transferring.

- **Workflows triggering unexpectedly**:
  - Disable "Assignee Changes" workflows before performing bulk transfers.
  - Check your workflow settings to see which automations might be affected.

- **Can't find Advanced Actions button**:
  - The Advanced Actions button is in the top toolbar of the Contacts list, separate from the Bulk Update button.
  - Ensure you have the necessary permissions to perform advanced actions.

## Best practice 💡
- **Test First**: Before performing bulk operations on large contact lists, test with a small group first.
- **Review Before Transfer**: Check how many contacts are assigned to the source assignee before transferring to avoid moving more contacts than intended.
- **Disable Workflows**: Temporarily disable assignee-related workflows before bulk transfers to prevent automation conflicts.
- **Use Tags Strategically**: Plan your tag structure before bulk adding tags to ensure consistent categorization.
- **Document Changes**: Keep track of bulk operations, especially assignee transfers, for team coordination and audit purposes.
- **Refresh After Operations**: Refresh the contacts list after bulk operations to see the updated results.

## Related Documentation
- [Contacts Overview](./index.md) - Learn about the Contacts module
- [Import & Export](./import-export.md) - Learn how to import and export contacts
