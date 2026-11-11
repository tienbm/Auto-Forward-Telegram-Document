---
description: Change a word, phrase, username, or link before a message is forwarded.
icon: wand-magic-sparkles
---

# Basic — Replace or Remove Text

Use **Basic** when you know the exact text you want to change. For example, replace an old username, update a link, or remove an unwanted phrase from forwarded messages.

### Create the rule

1. Open **Replace** from the Dashboard (mobile) or the Features menu (web), then select **Add New**.
2. Set **Replace Type** to **Basic**.
3. Enter a short **Label**, such as `update_contact`. Use letters, numbers, hyphens, or underscores; do not use spaces.
4. In **Original Words**, enter the text to find, for example `@old_contact`.
5. In **New Words Replace**, enter `@new_contact`. To remove the matching text, leave this field blank where supported. If your app requires a value before saving, enter `EMPTY`, the removal value shown in the advanced examples on the parent page.
6. If available, paste a sample message into **Full Content Original** to check the match.
7. Select the intended task under **Apply For Task**, then select **Create Replace**.

### Example

**Before:** Contact @old\_contact for details.

**Original Words:** `@old_contact`\
**New Words Replace:** `@new_contact`

**After:** Contact @new\_contact for details.

### Remove a phrase

To change `I do not like black.` to `I like black.`, enter `do not` in **Original Words**, including the trailing space, and use an empty replacement (or `EMPTY` if required by your app). Check surrounding spaces in the result.

### Replace the whole text

Use `[[FULL_TEXT]]` in **Original Words** to replace the original text with a new message. For example, set **New Words Replace** to `Shared from [[SOURCE_NAME]].` Shortcodes are filled in when the message is processed.

### Check the result

Make sure the rule is enabled for your intended task. Forward a sample message and check the destination. Replace does not work when **Show Header Forwarder** is enabled for the task.

If nothing changes, check the original text, punctuation, spaces, and task assignment. Clickable text or Premium emoji may contain hidden formatting; see the advanced examples on the parent Replace Content page. Use **Use Regex** when the text varies and you need to match a pattern.
