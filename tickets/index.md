# Tickets

## What is Tickets?

The Tickets module helps you track customer requests and internal tasks from start to finish. Each request becomes a ticket with a unique number, e.g. `SUP-12`. Tickets move through the stages of a pipeline until they are solved, so nothing gets lost in the chat.

{% hint style="info" %}
**Key Features**

- **Custom Pipelines**: Create a pipeline per team or request type, each with its own stages and ticket number prefix
- **Kanban Board**: Drag tickets between stages as work progresses
- **Collaboration**: Add collaborators, @mention teammates in comments and see the full change history
- **Public Links**: Share a read-only ticket page with customers or vendors
- **Contact Integration**: Link tickets to contacts and create them straight from the Inbox
- **Automation**: Create tickets automatically from message flows
- **Reporting**: Ticket volume, workload and breakdowns in the Tickets Report
{% endhint %}

## Core Features

{% columns %}
{% column %}
**Pipelines & Stages**
- Custom stages
- Solved (Done) stage
{% endcolumn %}

{% column %}
**Kanban Board**
- Drag-and-drop
- Filters & search
{% endcolumn %}

{% column %}
**Collaboration**
- Comments & @mentions
- Public ticket links
{% endcolumn %}

{% column %}
**Reporting**
- Team workload
- Category & tag breakdowns
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
      <td>The visual Kanban interface for managing active tickets, pipelines and stages</td>
      <td><a href="./board.md">./board.md</a></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>List</strong></td>
      <td>A searchable table of all tickets in a pipeline, plus archived tickets</td>
      <td><a href="./list.md">./list.md</a></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Tickets Report</strong></td>
      <td>Ticket volume, workload and breakdowns, under Reports</td>
      <td><a href="../reports/tickets.md">../reports/tickets.md</a></td>
      <td></td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
The **Summary** tab has moved. Ticket reports are now under `Reports` > `Tickets`. See [Tickets Report](../reports/tickets.md).
{% endhint %}

## Tickets across Luluchat

* **[Inbox > Contact Info > Tickets](../inbox/contact-info/tickets.md)**: See a contact's tickets and create a new one while chatting.
* **[Add to Ticket Stage](../automations/logics/actions/add-ticket-stage.md)**: Create a ticket automatically from a message flow, e.g. when a customer picks *Report a problem*.
* **[MCP Ticketing tools](../mcp/tools/ticketing.md)**: Let an AI assistant create, update and comment on tickets.

## Access and permissions

Admins control ticket access per user in `Settings` > `Users`, under **Ticketing Page**:

* **Has access to All Tickets**: The user sees every ticket.
* **Only has access to Assigned Tickets**: The user only sees tickets they work on.

{% hint style="warning" %}
The Tickets module is only available on plans that include ticketing. If you can't see **Tickets** in the left menu, check your plan or ask your admin for access.
{% endhint %}
