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
