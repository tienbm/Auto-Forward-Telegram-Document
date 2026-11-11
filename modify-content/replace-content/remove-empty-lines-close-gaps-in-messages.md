---
description: Remove blank lines while keeping the message text.
icon: wand-magic-sparkles
---

# Remove Empty Lines — Close Gaps in Messages

Use **Remove Empty Lines** to make a message more compact. It removes blank lines between paragraphs while keeping the lines that contain content.

### Create the rule

1. Open **Replace** from the Dashboard (mobile) or Features menu (web), then select **Add New** to open **Create Replace**.
2. Choose **Remove Empty Lines** under **Replace Type**.
3. Enter a short **Label**, such as `remove_gaps`.
4. The app configures the empty-line matching for this type. You do not need to enter a list of words to remove.
5. Choose the intended task under **Apply For Task**, then select **Create Replace**.

### Example

**Before:**

```
Order confirmed

Your parcel is ready.

Tracking will follow.
```

**After:**

```
Order confirmed
Your parcel is ready.
Tracking will follow.
```

Only the gaps disappear. The words and the order of the remaining lines stay the same.

### Check the result

Confirm that the saved rule is applied to the intended task, then forward a sample message and inspect the destination. Turn off **Show Header Forwarder** for tasks using Replace. To stop using the rule for a task, deactivate its task assignment in the Replace list; the saved rule remains available.

### When to choose another type

To remove a line containing an advert or other unwanted text, choose **Remove Lines By Keywords**. To remove fixed positions, choose **Remove Lines By Line Number**. A line containing invisible characters may behave differently from a truly blank line; test with a copy of your real source message.
