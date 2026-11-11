---
description: Keep matching lines and remove the rest of a message.
icon: wand-magic-sparkles
---

# Keep The Line Containing The Keyword — Keep Relevant Lines

Use **Keep The Line Containing The Keyword** when you only want selected information from a longer message. Lines containing one of your keywords stay; other lines are removed. The remaining lines keep their original order.

### Create the rule

1. Open **Replace** from the Dashboard (mobile) or Features menu (web), then select **Add New** to open **Create Replace**.
2. Set **Replace Type** to **Keep The Line Containing The Keyword**.
3. Enter a **Label**, such as `keep_delivery`.
4. Enter `Order:` as the first keyword.
5. Tap **+ New Keyword** and add `Delivery:`. Each additional keyword gives another way for a line to be kept.
6. Choose the intended task under **Apply For Task**, then select **Create Replace**.

### Example

**Keywords:** `Order:` and `Delivery:`

**Before:**

```
Daily summary
Order: A123
Internal note: ready for dispatch
Delivery: tomorrow
Follow our channel
```

**After:**

```
Order: A123
Delivery: tomorrow
```

The entire matching line stays, including any other words on that line. This is a line filter; it does not extract only the keyword.

### Check the result

Confirm that the saved rule is applied to the intended task, then forward a sample message and inspect the destination. Turn off **Show Header Forwarder** for tasks using Replace. To stop using the rule for a task, deactivate its task assignment in the Replace list; the saved rule remains available.

### If useful lines are missing

Make sure every line you need contains at least one of the keywords. Check spelling, spaces, and capitalization against a real sample. For example, keeping a Take Profit line does not automatically keep a Stop Loss line; add a keyword for each kind of line you need.

To remove matching lines and keep everything else, choose **Remove Lines By Keywords**.
