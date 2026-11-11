---
description: Group several simple or Regex replacements in one rule.
icon: wand-magic-sparkles
---

# Replace Power — Combine Multiple Replacements

Choose **Replace Power** when you need several changes in one message. Add a separate entry for each change and choose **Simple** or **Regex** for that entry.

### Create the rule

1. Open **Replace** from the Dashboard (mobile) or Features menu (web), then select **Add New** to open **Create Replace**.
2. Select **Replace Power** under **Replace Type**.
3. Enter a **Label**, such as `clean_updates`.
4. For the first replacement entry, select **Simple**. Enter `old brand` as the original text and `new brand` as its replacement.
5. Select **+ Add New Syntax** to add another entry.
6. For the second entry, select **Regex**. Enter `(good|perfect)` as the original pattern and `great` as the replacement.
7. Choose the intended task under **Apply For Task**, then select **Create Replace**.

### Example

**Entry 1 — Simple:** `old brand` → `new brand`

**Entry 2 — Regex:** `(good|perfect)` → `great`

**Before:** old brand has a good offer and perfect timing.

**After:** new brand has a great offer and great timing.

### Choose a mode for each entry

**Simple** finds the literal text you enter. Use it for a fixed word, phrase, or username.

**Regex** finds a pattern. Use it when a single entry should match several alternatives or changing text.

Enter each original/replacement pair in its own form entry. You do not need to combine everything into one long Regex. Start with a small number of entries and add more after checking the result.

### Check the result

Confirm that the saved rule is applied to the intended task, then forward a sample message and inspect the destination. Turn off **Show Header Forwarder** for tasks using Replace. To stop using the rule for a task, deactivate its task assignment in the Replace list; the saved rule remains available.

### If several changes interact

Check whether one entry creates text that another entry can match. Test the complete group with representative messages; do not assume independent changes when their text overlaps. For only one fixed change, **Basic** is simpler. For only one pattern, use **Use Regex**.
