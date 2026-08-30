---
icon: clone
---

# Clone Messages

### What it is

The Clone Profile flow has been improved to make it easier to create, open, review, and manage clone profiles.

This update focuses on smoother navigation, better list synchronization, and clearer handling when some cloned messages are still missing.

{% hint style="info" %}
### **Download Mobile App or use Web**

✅ **iOS** → [App Store](https://apps.apple.com/us/app/autoforward-for-telegram/id6447486093)\
✅ **Android** → [Google Play](https://play.google.com/store/apps/details?id=com.autoforward.telegramforward)\
✅ **Web** → [web.autoforwardtelegram.com](https://web.autoforwardtelegram.com/)
{% endhint %}

You can use this flow in the **Home** -> **Clone** area of the app.

<figure><img src="../.gitbook/assets/image (261).png" alt=""><figcaption></figcaption></figure>

### How to use it

1. Open **Clone Profile**.
2. Create a new clone profile.
3. Review the profile detail screen.
4. Start or manage clone operations from the profile.
5. Return to the list when needed. Your newly created profile should already be synced there.

### What is improved

* better create-to-detail flow
* more reliable list sync after creating a profile
* clone count badge on Home
* count cached per `userId`
* clearer handling for incomplete clone results

### Clone Again vs Retry Missing

These two actions serve different purposes:

* **Clone Again** starts a brand-new clone operation from the beginning.
* **Retry Missing** only retries messages that were not cloned successfully and are still retryable.

### Why it is useful

* It reduces confusion after creating a new clone profile.
* It helps your profile list stay up to date.
* It makes it easier to continue a partially completed clone instead of starting from scratch.
* It gives you a quicker overview of clone-related activity from Home.

### Example

If a large clone operation finishes with some missing messages, you may not need to rerun everything.

In that case:

* use **Retry Missing** if retryable messages are available
* use **Clone Again** only when you want to run the whole process again

#### Part1: Clone Messages from One Channel to Another&#x20;

{% embed url="https://youtu.be/iIlr8c7vDCQ" %}

#### Part2: Clone Messages from One Group to Group/Topics

{% embed url="https://youtu.be/ReIA8fNXk18" %}

### Date-wise Clone

Date-wise Clone adds a date heading before messages copied from each original day. This makes multi-day Telegram archives easier to browse.

```
📅 May 31, 2025
[messages from May 31]

📅 June 6, 2025
[messages from June 6]
```

The heading shows the original content date. It does not change Telegram's timestamp; cloned messages still show the time they are sent.

#### How to use it

1. Open **Clone** for a one-time run, or open **Clone Profiles** and tap **New profile** to save the setup.
2. Select **Source Chat Clone** and **Target Chat Clone**.
3. Under **Clone mode**, choose **By count** or **ID range**.
4. Enter **Start From Message ID**. In **ID range** mode, also enter **End ID (included)**.
5. Turn on **Date-wise clone**.
6. Optionally set **Delay Clone**.
7. For a one-time run, review the summary and tap **Start Clone**. For a saved profile, tap **Save profile**, then use **Run** whenever needed.

<figure><img src="../.gitbook/assets/image (335).png" alt=""><figcaption></figcaption></figure>

#### Important behavior

* **End ID (included)** is part of the selected range.
* An ID range can contain up to 100,000 source IDs, but the final message count may be lower because messages can be deleted, filtered, or skipped.
* The date uses the timezone configured for your account.
* Albums stay grouped. If an album crosses the selected range boundary, the whole album is skipped.
* Date headings are not counted as cloned messages.
* Date-wise Clone is off by default. Turning it off affects future runs only; it does not remove headings already sent to Telegram.
* Only one clone operation can run for an account at a time.

#### Status and background app

Use the profile status card to check progress. If it looks outdated after returning to AutoForward, open the profile and tap **Click to Refresh**.

Putting the app in the background does not intentionally stop an accepted clone. Live progress may pause until the app is opened again. Wait for the current run to finish before tapping **Run** again.

If a run finishes with **Completed with issues**, review the summary and use **Retry Missing** when available.

#### Change or stop a profile

* To change the setting, tap **Edit**, update **Date-wise clone**, then tap **Save profile**.
* To stop an active run, tap **Stop**. The status may briefly show **Stopping** while the current message finishes.
* To remove a saved setup, tap **Delete**. This does not delete messages from Telegram or remove previous run history.

#### If the result is not as expected

* No headings: confirm that **Date-wise clone** was enabled for the run you started.
* Fewer messages than expected: an ID range is an upper bound, not a guaranteed message count.
* Wrong date: check the timezone configured for your account.
* Cannot run: check your Telegram connection, target permissions, plan limits, and whether another clone is still active.
