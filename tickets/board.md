# Tickets: Board

## What is the Tickets Board?
The Board is a visual Kanban interface where you manage your day-to-day ticketing operations. Each ticket is represented as a card, and you can move them between columns (stages) as they progress.

## Managing the Board

### Creating a Pipeline
If you haven't created a pipeline yet, you will be prompted to create one.
1. Click **Create Ticketing Pipeline**.
2. Give your pipeline a title and define your initial stages.
3. **Pipeline Visibility**: Choose between:
   - **Public**: The system creates a publicly accessible URL for each ticket in this pipeline. Anyone with the link can view the ticket without logging in.
   - **Private**: Only internal team members can access tickets in this pipeline. Tickets require authentication to view.

📸 Screenshot placeholder:
> [Screenshot: Pipeline form showing visibility options with Public/Private dropdown]

### Working with Stages
- **Add Stage**: Scroll to the right of the board and click **Add Stage**.
- **Edit Stage**: Click the **Settings (gear)** icon on a stage header to rename or archive it.
- **Rearrange**: Drag and drop stage headers to change their order.

### Managing Ticket Cards
- **Create Ticket**: Click the **+ (Plus)** icon at the top of any stage column.
- **Move Ticket**: Click and hold a card, then drag it to a new stage.
- **View/Edit Ticket**: Click on a card to open the ticket details form.

## Filtering the Board
Use the top bar to filter which cards are visible:
- **Search Summary**: Search for tickets by their title or description.
- **Collaborators**: Filter by specific team members or "Unassigned".
- **Advanced Filters**: Click **Filters** to access deeper filtering by **Tags**, **Due Date**, **Ticket Number**, **Priority**, and **Creation/Update Dates**.

📸 Screenshot placeholder:
> [Screenshot: Tickets Kanban board with cards in various stages and filters active]

## The Ticket Form
When you open a ticket, you can manage:
- **Summary & Description**: The main details of the request.
- **Assignee & Collaborators**: Who is responsible for the ticket.
- **Tags**: Categories for easier searching.
- **Priority**: Mark the urgency of the task.
- **Due Date**: Set a deadline for resolution.
- **Activity Logs & Comments**: Track the history of changes and communicate internally.

## Public Link to Ticket

### What is Public Link?
When a pipeline is set to **Public** visibility, Luluchat automatically generates a publicly accessible URL for each ticket in that pipeline. This allows you to share tickets with external stakeholders (customers, partners, vendors) who don't have access to your Luluchat account.

### How it works
1. **Pipeline Setting**: When creating or editing a pipeline, set the "Pipeline visibility" to **Public**.
2. **Automatic Generation**: Once a pipeline is public, every ticket created in that pipeline automatically gets a unique public URL.
3. **No Authentication Required**: Anyone with the public link can view the ticket details, comments, and attachments without needing to log in to Luluchat.
4. **Sharing**: You can copy and share the public link with external parties via email, messaging apps, or embed it in other systems.

### When to use Public Links
- **Customer Support**: Share ticket links with customers so they can track the status of their requests.
- **External Collaboration**: Allow vendors, partners, or contractors to view relevant tickets without giving them full account access.
- **Status Updates**: Provide stakeholders with a way to check ticket progress without requiring them to log in.
- **Integration**: Embed ticket links in external systems or documentation.

### Important behavior to know
- **Pipeline-Level Setting**: The public link feature is enabled at the pipeline level. All tickets in a public pipeline get public links; you cannot make individual tickets public in a private pipeline.
- **Cannot Change After Creation**: Once a pipeline is created, you cannot change its visibility setting. Plan your pipeline structure accordingly.
- **Security Consideration**: Public links provide read-only access to ticket information. Anyone with the link can view the ticket, so only share links with trusted parties.
- **Link Format**: Public ticket URLs are unique and cannot be guessed. Each ticket has its own secure link.
- **Private Pipelines**: Tickets in private pipelines are only accessible to team members who are logged in to Luluchat.

### How to access Public Links
The public link for a ticket is typically available in the ticket details view. The exact location may vary, but it's usually displayed in the ticket form or details panel when viewing a ticket from a public pipeline.

📸 Screenshot placeholder:
> [Screenshot: Ticket details showing public link with copy button]

## Important behavior to know
- **Archiving**: You can archive tickets or entire stages to keep your board tidy without losing data.
- **Sync with Inbox**: You can create and view tickets directly from the **Contact Info** panel in the `Inbox`.
- **Pipeline Visibility**: Public pipelines generate shareable links for each ticket, while private pipelines restrict access to team members only.

## Best practice 💡
- **Keep it Updated**: Move tickets to the next stage as soon as the work is done to maintain an accurate view of the pipeline.
- **Use Priority**: Always set a priority for new tickets so the team knows what to tackle first.
