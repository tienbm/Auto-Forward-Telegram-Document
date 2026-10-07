---
icon: layer-plus
---

# Sticker Replace — Replace a Sticker with Text or Another Sticker

Sticker Replace changes a specific Telegram sticker into text or another sticker when forwarding messages. For example, you can turn a signal sticker into `CALL`, or replace a source sticker with one that suits your destination channel.

This feature is available in the mobile and web interfaces of AutoForward Messages.

### Replacement modes

<figure><img src="../../.gitbook/assets/image (345).png" alt=""><figcaption></figcaption></figure>

| Mode                  | Result                                                                |
| --------------------- | --------------------------------------------------------------------- |
| **Sticker → Text**    | Replaces the source sticker with your text, including multiple lines. |
| **Sticker → Sticker** | Replaces the source sticker with another sticker.                     |

Replace continues to process text by default. To replace stickers, select one of these modes under **Replace Type**.

### Before you start

* Have a forwarding task to which you want to apply the rule.
* Prepare the source sticker and, for **Sticker → Sticker**, the replacement sticker.
* Your account must meet the existing plan requirements for Replace.

### 1. Get the correct sticker ID

The two fields use different types of ID:

| Field                      | Required ID      | Purpose                            |
| -------------------------- | ---------------- | ---------------------------------- |
| **Source sticker ID**      | `file_unique_id` | Identifies the sticker to replace. |
| **Replacement sticker ID** | `file_id`        | Sends the replacement sticker.     |

1. Open [@FindMyIDs\_Bot in Telegram](https://t.me/FindMyIDs_Bot) and tap **Start**.
2. Forward the sticker you want to use to the bot.
3. Copy the `file_unique_id` value from the response for the source sticker.
4. If replacing it with another sticker, forward the replacement sticker and obtain its `file_id` value.

You can also tap the **ⓘ** icon beside an ID field title in the app to open the guide and its bot link.

{% hint style="info" %}
A `file_unique_id` identifies a sticker; it cannot send one. For the replacement sticker, the `file_id` must work with the Telegram account or bot that sends messages for your task. An ID obtained from one bot may not work with another sender.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (346).png" alt=""><figcaption></figcaption></figure>

### 2. Create a Sticker → Text rule

1. Open **Replace**, then open the **Create Replace** form.
2. Under **Replace Type**, select **Sticker → Text**.
3. Enter a **Label** to identify the rule, such as `sticker_call`.
4. Paste the `file_unique_id` into **Source sticker ID**. You can use the **Paste** button.
5. Enter your output text in **New Words Replace(\*)**, such as `CALL`.
6. Under **(Optional) Apply For Task**, select the task to which the rule should apply.
7. Tap **Create Replace**.

The output text must not be empty. Spaces and line breaks you enter are preserved. Sticker rules match the exact ID and do not use Regex or Ignore Case.

<figure><img src="../../.gitbook/assets/image (347).png" alt=""><figcaption></figcaption></figure>

### 3. Create a Sticker → Sticker rule

1. Open **Create Replace** and select **Sticker → Sticker**.
2. Enter a **Label**.
3. Paste the source sticker’s `file_unique_id` into **Source sticker ID**.
4. Paste the replacement sticker’s `file_id` into **Replacement sticker ID**.
5. Select the task and tap **Create Replace**.

Copy IDs exactly: do not change capitalization or add spaces or line breaks. Text → Sticker is not currently supported.

<figure><img src="../../.gitbook/assets/image (348).png" alt=""><figcaption></figcaption></figure>

### 4. Check the saved rule

The rule appears in **Replaces**, showing **Sticker → Text** or **Sticker → Sticker**, the source ID, and the replacement content.

Check the assigned task, then send a new sticker message to that task’s source and inspect the destination. Use a test task or chat to avoid affecting live content.

{% hint style="info" %}
Do not assume an empty task selection means the rule applies to all tasks. Check the assigned tasks in the list after saving.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (349).png" alt=""><figcaption></figcaption></figure>

### Manage a rule

* **Edit:** open the rule’s edit action, update the ID or output, and save. Check the saved content and assigned tasks afterward.
* **Enable or disable for a task:** use the actions in the Replace list to apply or stop applying the rule to a task. Stopping application does not delete the saved rule.
* **Delete:** use **Delete** when you no longer need the rule. This removes the rule from AutoForward, not the sticker from Telegram.

Rule changes apply to new source messages. Sticker → Sticker does not replace previously forwarded sticker media through the message-edit flow.

### Using Replace with sticker OCR

An applicable Sticker Replace rule takes priority over sticker OCR. If a sticker matches the rule, the task uses the replacement output. Text produced by Sticker → Text continues through the task’s normal content-processing flow.

### Troubleshooting

| Problem                                | What to check                                                                                            |
| -------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| The ID cannot be saved                 | The ID must be nonempty and contain no whitespace. Check that each field uses the correct ID type.       |
| The sticker is not replaced            | Check file\_unique\_id, assigned tasks, whether the rule is applied, and test with a new source message. |
| The replacement sticker cannot be sent | Check that file\_id works with the task’s sender. Do not use file\_unique\_id as the output.             |
| Access is denied because of your plan  | Check your account’s Replace entitlement.                                                                |
| Saving times out                       | Reopen the list to check whether the rule was created before creating it again, to avoid duplicates.     |

### Image checklist before publishing

| ID | Image to add            |
| -- | ----------------------- |
| 01 | In-app sticker ID guide |
| 02 | Sticker → Text form     |
| 03 | Sticker → Sticker form  |
| 04 | Saved rule card         |
