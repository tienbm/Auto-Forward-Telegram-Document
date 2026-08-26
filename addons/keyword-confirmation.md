---
icon: puzzle
---

# Keyword Confirmation

{% hint style="info" %}
### **Download Mobile App or use Web**

✅ **iOS** → [App Store](https://apps.apple.com/us/app/autoforward-for-telegram/id6447486093)\
✅ **Android** → [Google Play](https://play.google.com/store/apps/details?id=com.autoforward.telegramforward)\
✅ **Web** → [web.autoforwardtelegram.com](https://web.autoforwardtelegram.com/)
{% endhint %}

### 1. Overview

The Signal Confirmation add-on allows a task to forward a message only after its content has received enough confirmations based on configured words or hashtags.

This is useful for reducing noise and forwarding only information confirmed by multiple source messages.

### 2. How It Works

When enabled:

1. The system monitors configured words and hashtags across all sources in the task.
2. Each matching source message counts as one confirmation.
3. When the required number of confirmations is reached, the message completing the rule is forwarded.
4. After a successful forward, the rule pauses for the configured cooldown period.
5. Messages that do not meet the confirmation requirements are not forwarded by this rule.

You can create up to 10 rules.

### 3. Configuration Fields

| Field                  | Description                                                                       |
| ---------------------- | --------------------------------------------------------------------------------- |
| Enable Feature         | Turns signal confirmation on or off for the task                                  |
| Signal Name            | A name used to identify the rule, up to 50 characters                             |
| Words or Hashtags      | One or more words, phrases, or hashtags representing the same signal              |
| Match Style            | `literal`: matches text or phrases; `hashtag_exact`: matches one complete hashtag |
| Required Matches       | Number of matching messages required before forwarding, from 2 to 100             |
| Counting Period        | Time window in which matching messages are counted, from 5 minutes to 7 days      |
| Pause After Forwarding | Cooldown period after a successful forward, from 0 to 7 days                      |

Default values:

* Required matches: 10
* Counting period: 24 hours
* Pause after forwarding: 6 hours

### 4. Configuration Example

Create the following rule:

* Name: `Breaking News`
* Alias 1: `breaking news` — match style `literal`
* Alias 2: `#breaking` — match style `hashtag_exact`
* Required matches: `3`
* Counting period: `1 hour`
* Pause after forwarding: `6 hours`

Result:

* If 3 different source messages within 1 hour contain `breaking news` or the complete hashtag `#breaking`, the third matching message is forwarded.
* The same rule will not trigger again for 6 hours.

### 5. Recommendations

* For high-volume content, use 3–5 required matches within 30 minutes to 1 hour.
* For higher confidence, use 10 required matches within 24 hours.
* Use the cooldown period to prevent repeated forwarding of the same signal.
* For hashtags, always include the `#` symbol, for example `#bitcoin`.

Rule IDs and revisions are managed automatically by the backend. Users do not need to enter or edit them.
