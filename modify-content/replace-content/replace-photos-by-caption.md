---
icon: image-landscape
---

# Replace photos by caption

Automatically replace a source photo with one of your chosen photos when its caption matches a keyword or pattern. For example, forward a “Good morning” post using your channel’s own morning image.

**Requirements:** Platinum or Trial Platinum, and a forwarding task. Currently supports **single photos with captions only**. Albums, photos without captions, GIFs and photos sent as documents are excluded.

### 1. Get your replacement photo IDs

1. Send each replacement photo to [@FindMyIDs\_Bot](https://t.me/FindMyIDs_Bot).
2. Copy **`file_id`** from the response, not `file_unique_id`.
3. For multiple photos, collect each ID and separate them with commas in the app.

Tap **How to get file\_id** in the form to open the guide. Do not enter photo URLs or bot tokens in the ID field.

### 2. Create a rule

1. Open **Replaces** → **+** → **Create Replace**.
2. Tap **Replace Type** and choose **Replace photo by caption**.
3. Enter a **Label**, such as `morning`.
4. Choose **Photo selection**:
   * **In order:** use photos in list order, then start again from the first.
   * **Random:** select a photo randomly; repeats are possible.
5. Enter your keyword or pattern in **Caption pattern (Python regex)**.
6. Paste the IDs into **Photo file\_id list**.
7. Tap **Select Task**, choose the task to apply the rule to, then tap **Create Replace**.

Example caption pattern:

```
(?i)good morning|hello
```

This matches either phrase, ignoring letter case. Entering just `test` matches captions containing lowercase `test` and is case-sensitive.

Example ID format: `PHOTO_FILE_ID_A,PHOTO_FILE_ID_B`. These are placeholders; replace them with your actual photo IDs.

<figure><img src="../../.gitbook/assets/image (352).png" alt=""><figcaption></figcaption></figure>

### 3. Check the result

Make sure the task is running, then send **a single photo with a matching caption** to the source and check the destination. Saving the rule does not start the task or verify whether the IDs work with its sending account/bot.

If an older session has just been upgraded, use **Restart Bot** once before assigning its first photo rule. Later rule edits do not require this upgrade step.

The rule card shows its caption pattern, replacement photo count and selection mode.

<figure><img src="../../.gitbook/assets/image (353).png" alt=""><figcaption></figcaption></figure>

### Good to know

* This rule **replaces the photo**, not the caption text. Other text replacement rules still run normally.
* You can edit the caption pattern, photo IDs and selection mode. Changes affect new photo selections; earlier messages retain their selected photos.
* To stop applying the rule, remove its task assignment. Delete the rule when no longer needed.
* If the photo does not change, check the task assignment, supported source photo type and caption match. For unusable IDs, obtain new IDs and test with the task’s actual sending account/bot; an invalid ID does not fall back to the original photo.
