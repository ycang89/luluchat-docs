# Webhook

## What is Webhook?
Calls an external URL (GET/POST) from the flow, sending data and handling success/fail branches.

## When does it trigger?
- When the flow reaches this `Webhook` action while the flow is active and the channel is connected.

## How to set it up (Step by Step)

### Step 1: Open the flow and edit the Action node
In `Automations` > `Message Flows`, open a flow, select the `Action` step, and choose `Webhook`.

📸 Screenshot placeholder:
> [Screenshot: Action step showing the Webhook option]

### Step 2: Configure request details
Enter the URL, choose GET or POST, and add headers/parameters and any attributes to send. Define success/fail handling if available.

📸 Screenshot placeholder:
> [Screenshot: Webhook action form with URL, method, headers, params, and response paths]

## What happens after it triggers?
The webhook fires with your payload. The flow follows the success or fail path based on the response rule you set.

## Important behavior to know
- Ensure the endpoint accepts your method and payload format.
- Network or auth failures route to the fail path (if configured).
- Sensitive data should be handled securely in headers/params.

## Common issues & solutions
- Request failed: verify URL, method, required headers/auth, and that the endpoint is reachable.
- No follow-up: connect both success and fail paths to avoid dead ends.

## Best practice 💡
- Test with a small payload first; log responses on the receiving side.
- Use headers for auth tokens; avoid placing secrets in query strings.
