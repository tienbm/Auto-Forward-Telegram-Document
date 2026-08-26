---
description: >-
  Use OCR Image AI to detect a keyword inside an image, add a unique marker to
  the message content, and use Blacklist to skip the post automatically.
---

# Automatically Skip Telegram Posts with Image Keywords Using OCR AI

{% hint style="info" %}
### **Download Mobile App or use Web**

✅ **iOS** → [App Store](https://apps.apple.com/us/app/autoforward-for-telegram/id6447486093)\
✅ **Android** → [Google Play](https://play.google.com/store/apps/details?id=com.autoforward.telegramforward)\
✅ **Web** → [web.autoforwardtelegram.com](https://web.autoforwardtelegram.com/)
{% endhint %}

### What does this feature do?

This workflow is useful when you want to ignore posts that contain a specific word or phrase in an image.

For example, you can detect the English word `PROMOTION` and skip any post whose image contains that word:

1. OCR Image AI reads the image.
2. The custom prompt returns a unique marker.
3. **APPEND TO CAPTION** adds the marker to the forwarded message content.
4. **Blacklist** detects the marker and prevents the post from being forwarded.

Posts without the keyword continue through the forwarding workflow.

{% embed url="https://youtu.be/4BGoh7sRShU" %}

### Before you start

* Create or open the forwarding task that contains the source and destination chats.
* Prepare a clear test image containing the keyword `PROMOTION`.
* Use a unique marker that is unlikely to appear in normal captions.
* Allow a little extra time for OCR processing. The app notes that using AI may cause slight delays in message forwarding.

### 1. Enable OCR Image AI

Open the OCR settings for your forwarding task.

1. Turn on **OCR Image AI Enable**.
2. Select **Custom Prompt**.
3. Keep your preferred model selected in **Model**.

<figure><img src="../.gitbook/assets/image (293).png" alt=""><figcaption></figcaption></figure>

### 2. Add the keyword prompt

In **Prompt Request**, enter the following prompt:

```
Read the text in the image.

If the image contains the word "PROMOTION", regardless of capitalization, return exactly:

OCR_SKIP_PROMOTION

If the image does not contain the word "PROMOTION", return an empty response.

Return only the required result. Do not provide an explanation or any other text.
```

The prompt returns `OCR_SKIP_PROMOTION` only when the keyword is found. Using a unique marker makes the filter more precise than adding the common word `PROMOTION` directly to Blacklist.

### 3. Append the OCR result to the message

Under **Text Output Position**, select **APPEND TO CAPTION**.

This setting adds the text extracted from the image to the end of the forwarded message content. In this example, a matching image adds `OCR_SKIP_PROMOTION` to the content that Blacklist can inspect.

Click **Save & Apply**.

<figure><img src="../.gitbook/assets/image (294).png" alt=""><figcaption></figcaption></figure>

### 4. Add the marker to Blacklist

Open **Blacklist** in the same forwarding task and add this exact value:

```
OCR_SKIP_PROMOTION
```

Save the Blacklist settings.

Do not add `OCR_PASS` or other generic words to Blacklist. A unique marker reduces the risk of skipping unrelated posts.

<figure><img src="../.gitbook/assets/image (295).png" alt=""><figcaption></figcaption></figure>

### 5. Test the workflow

#### Test an image that contains the keyword

Send a new post to the source chat. Use a neutral caption and an image that clearly contains `PROMOTION`.

Expected result:

* OCR detects `PROMOTION`.
* The custom prompt returns `OCR_SKIP_PROMOTION`.
* **APPEND TO CAPTION** adds the marker to the message content.
* **Blacklist** matches the marker.
* The post is skipped and does not arrive in the destination chat.

#### Test an image without the keyword

Send another new post with an image that does not contain `PROMOTION`.

Expected result:

* The marker is not returned.
* Blacklist does not match.
* The post is forwarded normally.

Use new test posts for each check so that you can clearly identify the result of the current configuration.

<figure><img src="../.gitbook/assets/image (296).png" alt=""><figcaption></figcaption></figure>

### After setup

The task is ready to skip image posts that contain `PROMOTION`. The OCR setting and the Blacklist entry work together:

| Image content                | OCR result           | Blacklist result | Forwarding result |
| ---------------------------- | -------------------- | ---------------- | ----------------- |
| Contains `PROMOTION`         | `OCR_SKIP_PROMOTION` | Match            | Skipped           |
| Does not contain `PROMOTION` | Empty response       | No match         | Forwarded         |

### Manage the configuration

#### Change the keyword

To detect a different word:

1. Update the keyword and marker in **Prompt Request**.
2. Select **APPEND TO CAPTION**.
3. Click **Save & Apply**.
4. Replace the old marker in **Blacklist** with the new marker.
5. Test the new keyword with a new image.

For example, replace `PROMOTION` with `DISCOUNT` and `OCR_SKIP_PROMOTION` with `OCR_SKIP_DISCOUNT`.

#### Disable OCR filtering

Turn off **OCR Image AI Enable** when you no longer want the task to analyze images. If the Blacklist entry remains, remove it separately if you no longer need that filter.

#### Remove the filter but keep OCR

Remove `OCR_SKIP_PROMOTION` from **Blacklist**. OCR can remain enabled, but matching posts will no longer be skipped by this Blacklist rule.

### Common statuses

| Status                         | Meaning                                               | What to do                                                     |
| ------------------------------ | ----------------------------------------------------- | -------------------------------------------------------------- |
| OCR enabled                    | Image analysis is active for the task.                | Confirm the custom prompt and output position.                 |
| Custom Prompt selected         | OCR follows the instructions in **Prompt Request**.   | Check the keyword and marker spelling.                         |
| **APPEND TO CAPTION** selected | OCR output is added to the forwarded message content. | Keep this selected when Blacklist must inspect the OCR result. |
| Blacklist marker present       | Matching content is filtered.                         | Use the exact marker returned by the prompt.                   |

### Troubleshooting

#### A post containing the keyword is still forwarded

Check the following:

1. **OCR Image AI Enable** is turned on.
2. **Custom Prompt** is selected.
3. The keyword and marker are spelled exactly the same in the prompt and **Blacklist**.
4. **APPEND TO CAPTION** is selected.
5. You clicked **Save & Apply** after changing the OCR settings.
6. The test uses a new post and a clear image.

Allow a short delay for OCR processing before checking the destination chat.

#### Posts without the keyword contain unexpected OCR text

The model may return text even when the keyword is not present. Make the prompt stricter and require an empty response when there is no match. If your model cannot reliably return an empty response, use a non-blacklisted value such as `OCR_PASS`; note that this value may be appended to the forwarded caption.

#### OCR does not detect the keyword

Use an image with larger, sharper, high-contrast text. Avoid heavily blurred, rotated, or partially hidden words. Test the exact spelling used in the prompt.

#### Unrelated posts are skipped

Use a more distinctive marker, such as `OCR_SKIP_PROMOTION`, instead of adding a common word directly to Blacklist. Also check that normal captions do not already contain the marker.

### Frequently asked questions

#### Can I use a phrase instead of a single word?

Yes. Replace `PROMOTION` in the prompt with the phrase you want to detect and update the marker in **Blacklist**.

#### Do I need to add the keyword itself to Blacklist?

No. The recommended setup adds a unique OCR marker, such as `OCR_SKIP_PROMOTION`, to Blacklist. This helps prevent false matches in normal captions.

#### Will OCR slow down forwarding?

AI image processing may cause slight delays in message forwarding.

#### What happens when the OCR setting is disabled?

The task no longer uses OCR Image AI for this filter. The Blacklist rule is managed separately and can be removed if it is no longer needed.
