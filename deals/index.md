# Deals

## What is Deals?

The Deals module is designed to help you track your sales opportunities. It allows you to visualize your sales pipeline, track potential revenue, and manage the progress of every lead from initial contact to a closed deal.

{% hint style="info" %}
**Key Features**

- **Sales Pipelines**: Custom stages for your unique sales funnel, with Won and Lost stage types
- **Revenue Tracking**: Assign amounts and see stage totals at a glance
- **Contact Integration**: Link deals to contacts and create them straight from the Inbox
- **Automation**: Create or move deals from message flows, and start flows when a deal changes stage
- **Reporting**: Won/lost counts, pipeline health and monthly sales in the Deals Report
{% endhint %}

## Core Features

{% columns %}
{% column %}
**Sales Pipelines**
- Custom stages
- Won / Lost stage types
{% endcolumn %}

{% column %}
**Revenue Tracking**
- Assign amounts
- Totals per stage
{% endcolumn %}

{% column %}
**Contact Integration**
- Link to contacts
- Create from Inbox
{% endcolumn %}

{% column %}
**Reporting**
- Won & lost deals
- Monthly sales
{% endcolumn %}
{% endcolumns %}

## Module Structure

<table data-view="cards">
  <thead>
    <tr>
      <th></th>
      <th></th>
      <th data-hidden data-card-target data-type="content-ref"></th>
      <th data-hidden data-card-cover data-type="files"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Board</strong></td>
      <td>The visual Kanban interface for managing active sales opportunities</td>
      <td><a href="./board.md">./board.md</a></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>List</strong></td>
      <td>A detailed table view of all deals in your pipeline</td>
      <td><a href="./list.md">./list.md</a></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Deals Report</strong></td>
      <td>Sales performance and pipeline health, under Reports</td>
      <td><a href="../reports/deals.md">../reports/deals.md</a></td>
      <td></td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
The **Summary** tab has moved. Sales reports for your deals are now under `Reports` > `Deals`. See [Deals Report](../reports/deals.md).
{% endhint %}

## Deals in Automations

* **[Add to Deal Stage](../automations/logics/actions/add-deal-stage.md)**: Create a deal for a contact, or move their deal, from a message flow.
* **[Deal Stage trigger](../automations/steps/trigger.md)**: Start a message flow when a deal enters a stage, for example send a thank-you message when a deal is *Won*.
* **[Send Conversions API Event](../automations/logics/actions/send-conversions-api-event.md)**: Report won deals to Meta as a *Purchase* so your ads optimise on real sales.
