---
description: Replace a source sticker with a different sticker when forwarding.
icon: wand-magic-sparkles
---

# Sticker to Sticker — Swap a Specific Sticker

Choose **Sticker → Sticker** to use your own sticker in place of a specific source sticker. This is useful when your destination channel uses a different set of visual signals.

### Get the two IDs

1. Open [@FindMyIDs\_Bot](https://t.me/FindMyIDs_Bot) in Telegram and tap **Start**.
2. Send the **source sticker** and copy its `file_unique_id`.
3. Send the **replacement sticker** and copy its `file_id`.

**The IDs serve different purposes:** `file_unique_id` identifies what to match; `file_id` is used to send the replacement. The replacement ID must work with the Telegram account or bot that sends your task’s messages. An ID obtained from one bot may not work with another sender.

### Create the rule

1. Open **Replace** from the Dashboard (mobile) or Features menu (web), then select **Add New** to open **Create Replace**.
2. Select **Sticker → Sticker** under **Replace Type**.
3. Enter a **Label**, such as `swap_sticker`.
4. Paste the source `file_unique_id` into **Source sticker ID**.
5. Paste the replacement `file_id` into **Replacement sticker ID**. Preserve capitalization and do not add whitespace.
6. Choose the intended task under **Apply For Task**, then select **Create Replace**.

### Example

**Before:** the source sends sticker A.

**Rule:** match sticker A’s `file_unique_id` and send sticker B using its `file_id`.

**After:** the destination receives sticker B.

The rule targets a specific sticker, not every sticker in its pack. Regex and Ignore Case are not used for sticker IDs.

### Check the result

Confirm the task assignment, then send a **new** sticker A message to the source. Check that the destination receives sticker B. Saving does not prove the replacement ID works with your sender. Earlier forwarded sticker media is not replaced through message edits.

### Troubleshooting

**No match:** check the source `file_unique_id` and assigned task.

**The replacement cannot be sent:** make sure the output is a `file_id`, not a `file_unique_id`, and verify it with the task’s actual sender.

**Cannot save:** check that both IDs are present, contain no spaces or line breaks, and that your account has Replace access.

### Manage the rule

Edit to change either sticker ID. Deactivate the task assignment to stop replacing stickers while keeping the rule. This mode does not convert text messages into stickers. An applicable Sticker Replace rule takes priority over sticker OCR.
