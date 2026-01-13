# Add to Deal Stage

## What is Add to Deal Stage?

Places the contact into a chosen deal pipeline stage (and optional tags/collaborators) when this Action runs.

## When does it trigger?

* When the flow reaches this `Add to Deal Stage` action while the flow is active and you have Deals access.

## How to set it up (Step by Step)

{% stepper %}
{% step %}
#### Open the flow and edit the Action node

In `Automations` > `Message Flows`, open a flow, select the `Action` step, and choose `Add to Deal Stage`.

📸 Screenshot placeholder:

> \[Screenshot: Action step showing the Add to Deal Stage option]
{% endstep %}
{% endstepper %}

## What happens after it triggers?

The contact is added to the specified deal stage with the selected tags/collaborators; the flow continues.

## Important behavior to know

* Only available if Deals is enabled and you have permission.
* Ensure the pipeline and stage exist before selecting them.

## Common issues & solutions

* Stage not updated: confirm Deals access and that the action sits on the published path.
* Pipeline/stage missing: create or enable it in Deals, then return to the flow.

## Best practice 💡

* Standardize stage names across flows.
* Add relevant tags to make deal reporting and filters clearer.
