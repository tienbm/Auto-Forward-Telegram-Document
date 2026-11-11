---
description: Remove selected lines from messages that follow a consistent layout.
icon: wand-magic-sparkles
---

# Remove Lines By Line Number — Delete Fixed Positions

Use **Remove Lines By Line Number** when the unwanted content always appears in the same position, such as the second line of a standard message template.

### Create the rule

1. Open **Replace** from the Dashboard (mobile) or Features menu (web), then select **Add New** to open **Create Replace**.
2. Select **Remove Lines By Line Number** under **Replace Type**.
3. Enter a **Label**, such as `remove_line_2_5`.
4. In **Line Order**, enter `2,5` to remove the second and fifth lines. Separate multiple line numbers with commas. The first line is line 1.
5. Choose the intended task under **Apply For Task**, then select **Create Replace**.

### Example

**Before, with line numbers shown for explanation:**

```
1. Daily update
2. Promotional heading
3. Order received
4. Delivery tomorrow
5. Join our channel
6. Thank you
```

**Line Order:** `2,5`

**After:**

```
Daily update
Order received
Delivery tomorrow
Thank you
```

The line numbers above are explanatory labels, not text to add to your message.

### Check the result

Confirm that the saved rule is applied to the intended task, then forward a sample message and inspect the destination. Turn off **Show Header Forwarder** for tasks using Replace. To stop using the rule for a task, deactivate its task assignment in the Replace list; the saved rule remains available.

### If the wrong line disappears

Check the original message layout, including blank lines and inserted headings. A line is a line break in the message; text wrapping onto another screen row is not a new message line. Test with a real source message before applying the rule broadly. If line positions change from post to post, **Remove Lines By Keywords** may be easier to maintain.
