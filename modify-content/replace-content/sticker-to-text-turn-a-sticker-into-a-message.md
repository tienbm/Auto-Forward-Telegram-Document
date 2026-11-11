---
description: Replace a specific Telegram sticker with your own text.
icon: wand-magic-sparkles
---

# Sticker to Text — Turn a Sticker into a Message

Use **Sticker → Text** to forward a specific sticker as a text message. For example, turn a signal sticker into `CALL` so the destination receives readable text.

### Get the source sticker ID

1. Open [@FindMyIDs\_Bot](https://t.me/FindMyIDs_Bot) in Telegram and tap **Start**.
2. Send the sticker you want to replace.
3. Copy its `file_unique_id`. This identifies the exact source sticker.

Use `file_unique_id` for the source, not `file_id`. Copy the value exactly, without spaces or line breaks.

### Create the rule

1. Open **Replace** from the Dashboard (mobile) or Features menu (web), then select **Add New** to open **Create Replace**.
2. Under **Replace Type**, select **Sticker → Text**.
3. Enter a **Label**, such as `sticker_call`.
4. Paste the copied `file_unique_id` into **Source sticker ID**.
5. In **New Words Replace**, enter `CALL` or your preferred message. You can use multiple lines. The output must not be empty.
6. Choose the intended task under **Apply For Task**, then select **Create Replace**.

### Example

**Before:** a source message containing the sticker whose ID you entered.

**After:** a text message containing `CALL`.

A different sticker does not match this rule, even if it looks similar. Sticker matching uses the exact ID, without Regex or Ignore Case.

### Check the result

Check the task assignment in the Replace list. Send a **new** matching sticker to the task source and inspect the destination. Do not assume leaving the task selection empty applies the rule to all tasks.

### Troubleshooting

**Nothing changes:** check the source `file_unique_id`, the task assignment, and whether the rule is enabled.

**The form cannot be saved:** check that the label, source ID, and output text are present. Remove whitespace around the ID and check your account’s Replace entitlement.

**Sticker OCR is also enabled:** an applicable Sticker Replace rule takes priority. Text produced by this mode continues through the task’s normal content processing.

### Manage the rule

Edit the rule to change its source ID or output text. Deactivate its task assignment to stop using it while keeping the rule. After a save timeout, check the list before creating it again to avoid duplicates.
