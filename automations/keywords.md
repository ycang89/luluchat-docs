# Keywords

## What is Keywords?
Keywords trigger an automated reply or flow when a contact’s message matches the rule you set (e.g., contains, exact match, begins with). Each keyword links to a Message Flow so contacts get an immediate guided response.

## When does it trigger?
- When an incoming message meets the keyword condition (match type you chose) for the active channel.
- Only if the linked Message Flow is available and the channel is connected.

## Keyword match rules (how each condition works)
- `is` (exact match): message must match the keyword exactly.
- `contain`: message includes the keyword anywhere in the text.
- `contain all`: message includes every keyword you list (all must be present).
- `begin with`: message starts with the keyword.
- `end with`: message ends with the keyword.

## How to set it up (Step by Step)

### Step 1: Open Keywords
Go to `Automations` > `Keywords` to see your keyword list and linked flows.

📸 Screenshot placeholder:
> [Screenshot: Keywords page showing list with keywords and linked flows]

### Step 2: Add or edit a keyword
Use the page controls to add or edit a keyword entry, choose the match condition (e.g., contains, exact), and link it to the Message Flow you want to run.

📸 Screenshot placeholder:
> [Screenshot: Keyword form with fields for keywords, match condition, and flow selection]

### Step 3: Save and test
Save the keyword, then send a test message that matches the condition to confirm the linked flow starts.

📸 Screenshot placeholder:
> [Screenshot: Keyword list showing the new keyword linked to a flow]

## What happens after it triggers?
The linked Message Flow starts immediately, sending the configured steps and responses to the contact.

## Important behavior to know
- Matching follows the condition you select (contains, exact, begins with, etc.); choose the narrowest rule to avoid overlaps.
- Keywords require a linked flow; without it nothing will send.
- Keywords are channel-specific; ensure you’re in the right channel when testing.
- Export is available if you need a backup of the keyword list.

## Common issues & solutions
- No reply: confirm the keyword condition matches the test text and the linked flow is active.
- Wrong flow fired: check for overlapping keywords and adjust match type or rename to avoid clashes.
- Can’t see a keyword: refresh or ensure you have access to this channel’s automations.

## Best practice 💡
- Keep keywords distinct and short; use phrases for specific intents.
- Pair each keyword with a concise flow designed for that intent.
- Periodically export and review keywords to retire unused ones.
