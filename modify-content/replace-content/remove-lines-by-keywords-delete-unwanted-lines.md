---
description: Remove entire lines that contain a keyword you specify.
icon: wand-magic-sparkles
---

# Remove Lines By Keywords — Delete Unwanted Lines

Choose **Remove Lines By Keywords** to delete unwanted lines, such as promotional text or notes, while keeping the rest of the message. A matching keyword removes the **whole line**, not just the keyword.

### Create the rule

1. Open **Replace** from the Dashboard (mobile) or Features menu (web), then select **Add New** to open **Create Replace**.
2. Select **Remove Lines By Keywords** under **Replace Type**.
3. Enter a **Label**, such as `remove_ads`.
4. In **Keywords**, enter `Sponsored`.
5. Use **+ New Keyword** to add another keyword, such as `Join our`. A line containing any of the listed keywords is removed.
6. Choose the intended task under **Apply For Task**, then select **Create Replace**.

### Example

**Keywords:** `Sponsored` and `Join our`

**Before:**

```
Product update
Sponsored: visit our partner
Version 2 is available.
Join our promotion channel
```

**After:**

```
Product update
Version 2 is available.
```

Both matching lines are removed. The title and update line remain.

### Check the result

Confirm that the saved rule is applied to the intended task, then forward a sample message and inspect the destination. Turn off **Show Header Forwarder** for tasks using Replace. To stop using the rule for a task, deactivate its task assignment in the Replace list; the saved rule remains available.

### Avoid removing useful content

Choose a distinctive keyword or phrase. A short keyword may also occur in a useful line. Test your actual source messages, including capitalization. To keep only matching lines, choose **Keep The Line Containing The Keyword** instead. To remove only a word from a line, use **Basic**.
