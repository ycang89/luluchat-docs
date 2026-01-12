# Logic: Randomizer

## What is the Randomizer Node?
The Randomizer allows you to split your traffic into different paths based on random probability. This is primarily used for A/B testing and experimentation.

## When does it trigger?
This node triggers every time a contact reaches it in a Message Flow. The system instantly performs a "roll of the dice" based on your configured percentages to decide which path the contact will follow.

## How to set it up (Step by Step)

### Step 1: Add the Randomizer Node
In the Message Flow Editor, click **Add Node (+) > Logics > Randomizer**.

📸 Screenshot placeholder:
> [Screenshot: Add Node menu with Logics > Randomizer selected]

### Step 2: Create your Variants
Click the node to open the configuration. Click **+ Add New Variant** to create multiple paths (e.g., Path A, Path B).

📸 Screenshot placeholder:
> [Screenshot: Randomizer configuration drawer with the 'Add New Variant' button]

### Step 3: Assign Percentages
Enter a **Probability %** for each variant.
**CRITICAL**: The total of all variants must equal exactly **100%**.

📸 Screenshot placeholder:
> [Screenshot: Variant list with 50% and 50% inputs]

### Step 4: Link to Next Steps
For each variant (A, B, C, etc.), click **Choose Next Step** to link it to a different message or action node on the board.

📸 Screenshot placeholder:
> [Screenshot: Randomizer node on the board with arrows pointing to different message nodes]

## What happens after it triggers?
The contact is silently routed to one of the available paths. There is no visible delay or notification to the customer that they have been part of a randomized split.

## Important behavior to know
- **True Randomness**: Each contact entering the node has a random chance of falling into any of the paths. Over a large number of contacts, the distribution will match your configured percentages.
- **No Memory**: If a contact enters the same randomizer twice (e.g., in a looping flow), they may be assigned a different path each time.
- **Max Variants**: You can add up to 6 different variants (A through F).

## Common issues & solutions
- **Total not 100%**: The editor will show an error if your total distribution doesn't sum to exactly 100. Double-check your math!
- **One path gets more traffic**: Over small groups, randomness can seem uneven. The percentages become statistically accurate as more contacts pass through the node.

## Best practice 💡
- **Simple A/B Test**: Start with two variants at 50% each to test which of two promotional offers gets a better response rate.
- **Test Content**: Use the Randomizer to see if using emojis in your initial greeting leads to higher engagement.
